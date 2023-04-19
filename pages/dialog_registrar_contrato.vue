<template>
  <v-app>


    <v-navigation-drawer app>
      <v-list-item class="text-center my-1 py-1">
        <v-list-item-content>
          <v-list-item-title class="text-h6"> Handra </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list dense nav active-class="deep-purple--text text--accent-4">
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-list-item-title class="font-weight-bold">Inicio</v-list-item-title>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>
          <v-list-item-title class="font-weight-bold">Registro</v-list-item-title>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-folder-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Local</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Cliente</v-list-item-title>
          </v-list-item>
          <v-list-item-title class="font-weight-bold">Catálogo</v-list-item-title>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-list-box</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Inventario</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-hammer-wrench</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Mantenimiento</v-list-item-title>
          </v-list-item>

          <v-list-item-title class="font-weight-bold">Información</v-list-item-title>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Administrador</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-box-multiple</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Clientes</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home-group</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold">Locales</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <template v-slot:append>
        <div class="pa-2">
          <v-btn block> Logout <v-icon dark right> mdi-logout </v-icon></v-btn>
        </div>
      </template>
    </v-navigation-drawer>

    <v-main>
      <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="80%">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              Open Dialog
            </v-btn>
          </template>

          <v-card elevation='10' rounded='xl'>
            <v-card-title>
              <h1 style="margin: 20px;">Registrar Contrato</h1>
            </v-card-title>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Contrato</h3>
                    </div>
                    <v-text-field label="Contrato" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Tipo de Contrato</h3>
                    </div>
                    <v-text-field label="Tipo de Contrato" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Propiedad</h3>
                    </div>
                    <v-text-field label="Propiedad" outlined dense></v-text-field>
                  </v-col>

                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Fecha del contrato</h3>
                    </div>

                    <v-menu ref="menu" v-model="menu" :close-on-content-click="false" :return-value.sync="date"
                      transition="scale-transition" offset-y min-width="auto">
                      <template v-slot:activator="{ on, attrs }">
                        <v-text-field v-model="date" label="Selecciona fecha de creación" prepend-icon="mdi-calendar"
                          readonly v-bind="attrs" v-on="on"></v-text-field>
                      </template>
                      <v-date-picker v-model="date" no-title scrollable>
                        <v-spacer></v-spacer>
                        <v-btn text color="primary" @click="menu = false">
                          Cancel
                        </v-btn>
                        <v-btn text color="primary" @click="$refs.menu.save(date)">
                          OK
                        </v-btn>
                      </v-date-picker>
                    </v-menu>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Fecha de Inicio</h3>
                    </div>

                    <v-menu ref="menu2" v-model="menu2" :close-on-content-click="false" :return-value.sync="date2"
                      transition="scale-transition" offset-y min-width="auto">
                      <template v-slot:activator="{ on, attrs }">
                        <v-text-field v-model="date2" label="Selecciona fecha de inicio" prepend-icon="mdi-calendar"
                          readonly v-bind="attrs" v-on="on"></v-text-field>
                      </template>
                      <v-date-picker v-model="date2" no-title scrollable>
                        <v-spacer></v-spacer>
                        <v-btn text color="primary" @click="menu2 = false">
                          Cancel
                        </v-btn>
                        <v-btn text color="primary" @click="$refs.menu2.save(date2)">
                          OK
                        </v-btn>
                      </v-date-picker>
                    </v-menu>


                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Fecha de Finalización</h3>
                    </div>
                    <v-menu ref="menu3" v-model="menu3" :close-on-content-click="false" :return-value.sync="date3"
                      transition="scale-transition" offset-y min-width="auto">
                      <template v-slot:activator="{ on, attrs }">
                        <v-text-field v-model="date3" label="Selecciona fecha de fin" prepend-icon="mdi-calendar" readonly
                          v-bind="attrs" v-on="on"></v-text-field>
                      </template>
                      <v-date-picker v-model="date3" no-title scrollable>
                        <v-spacer></v-spacer>
                        <v-btn text color="primary" @click="menu3 = false">
                          Cancel
                        </v-btn>
                        <v-btn text color="primary" @click="$refs.menu3.save(date3)">
                          OK
                        </v-btn>
                      </v-date-picker>
                    </v-menu>

                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Depósito</h3>
                    </div>
                    <v-text-field label="Depósito" outlined dense></v-text-field>
                  </v-col>

                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Arrendatario</h3>
                    </div>
                    <v-text-field label="Arrendatario" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Duración</h3>
                    </div>
                    <v-text-field label="Duración" outlined dense>

                    </v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Fotos</h3>
                    </div>
                    <v-file-input label="Fotos" outlined multiple state chips hint dense></v-file-input>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>

            <v-card-actions>
              <div class="mx-auto text-center">
                <v-btn rounded color="red" dark @click="dialog = false" style="margin : 10px">
                  <v-icon>mdi-close</v-icon>
                  Cancelar
                </v-btn>
              </div>
              <div class="mx-auto text-center">
                <v-btn rounded color="primary" dark @click="dialog = false" style="margin : 10px ">
                  <v-icon>mdi-plus</v-icon>
                  Guardar
                </v-btn>
              </div>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    dialog: false,

  }),
  dates: {
    date: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
    date2: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
    date3: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
    menu: false,
    menu2: false,
    menu3: false,

  },
}


</script>