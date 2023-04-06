<template>
  <v-app>
    <v-navigation-drawer app>
      <v-list-item class="text-center my-1 py-1">
        <v-list-item-content>
          <v-list-item-title class="text-h6"> Handras </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list dense nav active-class="deep-purple--text text--accent-4">
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item-title class="font-weight-bold">Inicio</v-list-item-title>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>
          <v-list-item-title class="font-weight-bold"
            >Registro</v-list-item-title
          >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-folder-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Local</v-list-item-title
            >
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Cliente</v-list-item-title
            >
          </v-list-item>
          <v-list-item-title class="font-weight-bold"
            >Catálogo</v-list-item-title
          >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-list-box</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Inventario</v-list-item-title
            >
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-hammer-wrench</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Mantenimiento</v-list-item-title
            >
          </v-list-item>

          <v-list-item-title class="font-weight-bold"
            >Información</v-list-item-title
          >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Administrador</v-list-item-title
            >
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-box-multiple</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Clientes</v-list-item-title
            >
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home-group</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="font-weight-bold"
              >Locales</v-list-item-title
            >
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
        <v-card class="mx-4 mt-8" width="300" height="300">
          <v-card flat>
            <v-img
              height="150"
              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
            >
            </v-img>

            <v-btn color="success" disable fab dark absolute bottom right>
              <v-icon>mdi mdi-lock-open-variant</v-icon>
            </v-btn>
          </v-card>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-domain</v-icon>
            </v-list-item-icon>
            <v-card-title>
              <span class="text-h6 font-weight-light">Starbucks</span>
            </v-card-title>
          </v-list-item>

          <v-card-text>
            <div class="my- 2 font-weight-black">Precio: $23,000</div>

            <div class="my-2 text--primary">Ubicacion: Piso 1:A3</div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 mt-8" width="300">
          <v-card flat class="d-flex justify-center">
            <v-avatar size="188">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>

            <v-btn color="success" disable fab dark absolute bottom>
              <v-icon>mdi mdi-lock-open-variant</v-icon>
            </v-btn>
          </v-card>
        </v-card>
      </v-row>
      <v-row class="mx-4">
        <v-card class="mx-4 mt-8" width="300" height="300">
          <v-card flat>
            <v-img
              height="150"
              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
            >
            </v-img>

            <v-btn color="error" disable fab dark absolute bottom right>
              <v-icon>mdi-lock</v-icon>
            </v-btn>
          </v-card>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-domain</v-icon>
            </v-list-item-icon>
            <v-card-title>
              <span class="text-h6 font-weight-light">Starbucks</span>
            </v-card-title>
          </v-list-item>

          <v-card-text>
            <div class="my- 2 font-weight-black">Precio: $23,000</div>

            <div class="my-2 text--primary">Ubicacion: Piso 1:A3</div>
          </v-card-text>
        </v-card>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
