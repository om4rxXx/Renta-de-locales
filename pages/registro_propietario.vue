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
      <v-row class="mx-4">
        <v-col class="mx-auto text-end">
          <v-container fluid style="height: 50px">

            <v-menu bottom min-width="50px" rounded offset-y>
              <template v-slot:activator="{ on }">
                <v-btn icon x-large v-on="on">
                  <v-avatar size="50px">
                    <img v-if="user.image" alt="Avatar" src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                    <v-icon v-else :color="message.color" v-text="message.icon"></v-icon>
                  </v-avatar>
                </v-btn>
              </template>
              <v-card>
                <v-list-item-content class="justify-center">
                  <div class="mx-auto text-center">
                    <v-avatar size="50px">
                      <img v-if="user.image" alt="Avatar"
                        src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                      <v-icon v-else :color="message.color" v-text="message.icon"></v-icon>
                    </v-avatar>
                    <h3>{{ user.fullName }}</h3>
                    <p class="text-caption mt-1">
                      {{ user.email }}
                    </p>
                    <v-divider class="my-3"></v-divider>
                    <v-btn depressed rounded text>
                      Edit Account
                    </v-btn>
                    <v-divider class="my-3"></v-divider>
                    <v-btn depressed rounded text>
                      Disconnect
                    </v-btn>
                  </div>
                </v-list-item-content>
              </v-card>
            </v-menu>
          </v-container>
        </v-col>
      </v-row>
      <v-row class="mx-4" justify="left">
        <v-col>
          <span class="text-h3">Registrar Propietario</span>
        </v-col>
      </v-row>
      <v-row class="mx-auto text-center" style="width: 90%;">
        <v-col>
          <v-card elevation='10' rounded='xl'>
            <v-card-title>
            </v-card-title>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Nombre</h3>
                    </div>
                    <v-text-field label="Nombre" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Apellido Paterno</h3>
                    </div>
                    <v-text-field label="Apellido Paterno" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Apellido Materno</h3>
                    </div>
                    <v-text-field label="Apellido Materno" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Correo Electrónico</h3>
                    </div>
                    <v-text-field label="Correo Electrónico" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Teléfono</h3>
                    </div>
                    <v-text-field label="Teléfono" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Dirección</h3>
                    </div>
                    <v-text-field label="Dirección" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">RFC</h3>
                    </div>
                    <v-text-field label="RFC" outlined dense></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%;">Tipo de Propietario</h3>
                    </div>
                    <v-text-field label="Tipo de Propietario" outlined dense></v-text-field>
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
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>
  
<script>
export default {
  name: "IndexPage",
};
</script>

<script>
export default {
  data: () => ({
    user: {
      image: 'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
      fullName: 'John Doe',
      email: 'john.doe@doe.com',
    },
  }),
}
</script>

