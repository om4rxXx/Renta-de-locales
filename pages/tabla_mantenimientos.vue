<template>
  <v-app>
    <Nav></Nav>
    <v-main>
      <Header></Header>
      <v-row class="mx-4" justify="left">
        <v-col>
          <span class="text-h3">Reporte de Mantenimientos</span>
        </v-col>
      </v-row>

      <v-row class="mx-auto text-center" style="width: 90%;">
        <v-col>

          <v-data-table :headers="headers" :items="mantenimientos" :search="search" sort-by="id" class="elevation-1">
            <template v-slot:top>
              <v-toolbar flat>
                <v-dialog v-model="dialog" max-width="50%">
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn rounded color="primary" dark class="mb-2" v-bind="attrs" v-on="on">
                      <v-icon>mdi-plus</v-icon>
                      Agregar
                    </v-btn>
                  </template>
                  <v-card rounded='xl'>
                    <v-card-title>
                      <span class="text-h5">{{ formTitle }}</span>
                    </v-card-title>

                    <v-card-text>
                      <v-container>
                        <v-row>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.tipo_mant" label="Tipo de Mantenimiento"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.descripcion" label="Descripción"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.proovedor" label="Proovedor"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.propiedad" label="Propiedad"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.fecha_crea" label="Fecha de Creación"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.fecha_mant" label="Fecha para Mantenimiento"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6" md="4">
                            <v-text-field v-model="editedItem.precio" label="Precio"></v-text-field>
                          </v-col>

                          <v-col cols="12" sm="6" md="4">

                          </v-col>
                        </v-row>
                      </v-container>
                    </v-card-text>

                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="blue darken-1" text @click="close">
                        Cancel
                      </v-btn>
                      <v-btn color="blue darken-1" text @click="save">
                        Save
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
                <v-spacer></v-spacer>
                <v-spacer></v-spacer>
                <v-spacer></v-spacer>
                <v-spacer></v-spacer>
                <v-text-field v-model="search" append-icon="mdi-magnify" label="Buscar mantenimiento" single-line
                  hide-details></v-text-field>
                <v-dialog v-model="dialogDelete" max-width="500px">
                  <v-card>
                    <v-card-title class="text-h5">¿Seguro de eliminar el registro?</v-card-title>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="blue darken-1" text @click="closeDelete">Cancel</v-btn>
                      <v-btn color="blue darken-1" text @click="deleteItemConfirm">OK</v-btn>
                      <v-spacer></v-spacer>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
                     </v-toolbar>

            </template>
            <template v-slot:item.actions="{ item }">
              <v-row >
                <v-col cols="2" sm="6" md="6" align="center" justify="center">
              <v-icon small class="mr-2" @click="editItem(item)">
                mdi-pencil
              </v-icon>
            </v-col>
            <v-col cols="2" sm="6" md="6" align="center" justify="center">
              <v-icon small @click="deleteItem(item)">
                mdi-delete
              </v-icon>
              </v-col>
              </v-row>
            </template>
            <template v-slot:no-data>
              <v-btn color="primary" @click="initialize">
                Reset
              </v-btn>
            </template>
            <template v-slot:item.estado="{ item }">
              <v-switch v-model="item.estado" inset v-if="item.estado == false" ></v-switch>
              <v-switch v-model="item.estado" inset v-else-if="item.estado == true" color=#4CAF50 disabled></v-switch>
            </template>
          </v-data-table>

        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>
 
<style>
.v-input--switch--inset,
.v-input--switch:not(.v-input--switch--flat) .v-input--switch__thumb {
  color: #FF9800
}

.theme--light.v-input--switch .v-input--switch__track {
  color: #FF9800
}
</style>
<script>
import Nav from "../components/Nav.vue";
import Header from "../components/Header.vue";

export default {
  name: "IndexPage",
  data: () => ({
    user: {
      image: 'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
      fullName: 'John Doe',
      email: 'john.doe@doe.com',

    },
    dialog: false,
    dialogDelete: false,
    dialogConfirmComplete : false,
    search: '',
    headers: [
      {
        text: 'ID',
        align: 'start',
        filterable: true,
        value: 'id',
      },
      { text: 'Tipo de Mantenimiento', filterable: true, value: 'tipo_mant', },
      { text: 'Descripción', filterable: false, value: 'descripcion' },
      { text: 'Proovedor', value: 'proovedor' },
      { text: 'Propiedad', value: 'propiedad' },
      { text: 'Fecha de Creación', filterable: true, value: 'fecha_crea' },
      { text: 'Fecha para mantenimiento', filterable: true, value: 'fecha_mant' },
      { text: 'Precio', filterable: false, value: 'precio' },
      { text: 'Estado', filterable: false, value: 'estado' },
      { text: 'Opciones', value: 'actions', sortable: false },
    ],
    mantenimientos: [],
    editedIndex: -1,
    editedItem: {

      tipo_mant: '',
      descripcion: '',
      proovedor: '',
      propiedad: '',
      fecha_crea: '',
      fecha_mant: '',
      precio: '',
      estado: false,
    },
    defaultItem: {

      tipo_mant: '',
      descripcion: '',
      proovedor: '',
      propiedad: '',
      fecha_crea: '',
      fecha_mant: '',
      precio: '',
      estado: false,
    },
  }),

  computed: {
    formTitle() {
      return this.editedIndex === -1 ? 'Agregar Mantenimiento' : 'Editar Mantenimiento'
    },
  },

  watch: {
    dialog(val) {
      val || this.close()
    },
    dialogDelete(val) {
      val || this.closeDelete()
    },
  },

  created() {
    this.initialize()
  },

  methods: {
    initialize() {
      this.mantenimientos = [
        {
          id: 1,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 3',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: false,
        },
        {
          id: 2,
          tipo_mant: 'Correctivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 3',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: false,
        },
        {
          id: 3,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 3',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: false,
        },
        {
          id: 4,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 11',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: false,
        },
        {
          id: 5,
          tipo_mant: 'Correctivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 3',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: false,
        },
        {
          id: 6,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 7',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: true,
        },
        {
          id: 7,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 7',
          fecha_crea: '14/02/2050',
          fecha_mant: '14/03/2050',
          precio: '$50.00',
          estado: true,
        },
        {
          id: 8,
          tipo_mant: 'Correctivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 3',
          fecha_crea: '14/04/2020',
          fecha_mant: '14/04/2020',
          precio: '$50.00',
          estado: true,
        },
        {
          id: 9,
          tipo_mant: 'Preventivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 4',
          fecha_crea: '14/06/2080',
          fecha_mant: '14/07/2080',
          precio: '$50.00',
          estado: true,
        },
        {
          id: 10,
          tipo_mant: 'Correctivo',
          descripcion: 'Se descompuso el lavamanos y se hizo cambio de tuberías',
          proovedor: 'Ferretería El triangulo',
          propiedad: 'Local 4',
          fecha_crea: '14/12/2050',
          fecha_mant: '14/12/2050',
          precio: '$50.00',
          estado: true,
        },
      ]
    },

    editItem(item) {
      this.editedIndex = this.mantenimientos.indexOf(item)
      this.editedItem = Object.assign({}, item)
      this.dialog = true
      this.editedItem.id = this.lastMant

    },

    deleteItem(item) {
      this.editedIndex = this.mantenimientos.indexOf(item)
      this.editedItem = Object.assign({}, item)
      this.dialogDelete = true
    },

    deleteItemConfirm() {
      this.mantenimientos.splice(this.editedIndex, 1)
      this.closeDelete()
    },

    close() {
      this.dialog = false
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem)
        this.editedIndex = -1
      })
    },

    closeDelete() {
      this.dialogDelete = false
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem)
        this.editedIndex = -1
      })
    },

    save() {
      if (this.editedIndex > -1) {
        Object.assign(this.mantenimientos[this.editedIndex], this.editedItem)

      } else {
        this.mantenimientos.push(this.editedItem)

      }
      this.close()
    },
  },
}
</script>

