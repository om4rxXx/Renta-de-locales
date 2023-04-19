

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

        <v-dialog v-model="dialog" persistent max-width="70%">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              Open Dialog
            </v-btn>
          </template>

          <v-card elevation='10' rounded='xl'>
            <v-card-title>
              <h1 style="margin: 20px;">Editar Propietario</h1>
            </v-card-title>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols ="2"  sm="6" md="4" align="center">
                    <v-row>
                      <v-col cols="1" sm="6" md="12" align="center">
                        <v-avatar size="200px">
                          <img v-if="user.image" alt="Avatar"
                            src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                        </v-avatar>
                        <v-row>
                          <v-col cols="1" sm="6" md="12" align="center">
                            <v-btn color="primary" fab large dark :loading="isSelecting" @click="onButtonClick">
                              <v-icon>mdi-pencil</v-icon>
                              {{ buttonText }}
                            </v-btn>
                            <input ref="uploader" class="d-none" type="file" accept="image/*" @change="onFileChanged">
                          </v-col>
                        </v-row>
                      </v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12">
                        <v-card-actions>
                          <div class="mx-auto text_left">
                            <v-btn rounded color="red" dark @click="dialog = false" style="margin : 10px">
                              <v-icon>mdi-close</v-icon>
                              Cancelar
                            </v-btn>
                          </div>
                          <div class="mx-auto text-left">
                            <v-btn rounded color="primary" dark @click="dialog = false" style="margin : 10px ">
                              <v-icon>mdi-plus</v-icon>
                              Guardar
                            </v-btn>
                          </div>
                        </v-card-actions>
                      </v-col>
                    </v-row>
                  </v-col>
                  <v-col cols ="2"  sm="6" md="8" align="center">
                    <v-row>
                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Nombre</h3>
                        </div>
                        <v-text-field label="Nombre" outlined dense></v-text-field>
                      </v-col>
                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Apellido Paterno</h3>
                        </div>
                        <v-text-field label="Apellido Paterno" outlined dense> </v-text-field>
                      </v-col>

                      <v-col cols="12" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Apellido Materno</h3>
                        </div>
                        <v-text-field label="Apellido Materno" outlined dense></v-text-field>
                      </v-col>

                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Correo Electrónico</h3>
                        </div>
                        <v-text-field label="Correo Electrónico" outlined dense> </v-text-field>
                      </v-col>

                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Teléfono</h3>
                        </div>
                        <v-text-field label="Teléfono" outlined dense> </v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Dirección</h3>
                        </div>
                        <v-text-field label="Dirección" outlined dense> </v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">RFC</h3>
                        </div>
                        <v-text-field label="RFC" outlined dense> </v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Tipo de propietario</h3>
                        </div>
                        <v-text-field label="Tipo" outlined dense> </v-text-field>
                      </v-col>
                      <v-col cols="12" sm="6" md="12">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Comentarios</h3>
                        </div>
                        <v-text-field label="Comentarios" outlined dense> </v-text-field>
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>

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
    user: {
      image: 'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
      fullName: 'John Doe',
      email: 'john.doe@doe.com',
    },
    selectedFile: null,
    isSelecting: false
  }),
  computed: {
    buttonText() {
      return this.selectedFile
        ? this.selectedFile.name
        : this.defaultButtonText;
    }
  },
  methods: {
    onButtonClick() {
      this.isSelecting = true;
      window.addEventListener(
        "focus",
        () => {
          this.isSelecting = false;
        },
        { once: true }
      );

      this.$refs.uploader.click();
    },
    onFileChanged(e) {
      this.selectedFile = e.target.files[0];

      // do something
    }
  }
}
</script>

