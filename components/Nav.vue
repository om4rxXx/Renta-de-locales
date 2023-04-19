<template>
  <v-navigation-drawer app>
    <v-card class="mx-auto" max-width="434" tile>
      <v-img
        height="100%"
        src="https://cdn.vuetifyjs.com/images/cards/server-room.jpg"
      >
        <v-row align="end" class="fill-height">
          <v-col align-self="center" class="pl-5 pt-5 pb-0" cols="12">
            <v-avatar class="profile" color="grey" size="80">
              <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
            </v-avatar>
          </v-col>
          <v-col class="py-0">
            <v-list-item color="rgba(0, 0, 0, .4)" dark>
              <v-list-item-content>
                <v-list-item-title class="text-h6">
                  Marcus Obrien
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-col>
        </v-row>
      </v-img>
    </v-card>

    <v-list dense nav active-class="deep-purple--text text--accent-4">
      <v-list-item-group
        v-model="group"
        active-class="purple-gradient white--text"
      >
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
          <v-list-item-title class="font-weight-bold"
            >Cliente</v-list-item-title
          >
        </v-list-item>
        <v-list-item-title class="font-weight-bold">Catálogo</v-list-item-title>
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
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style >
.v-progress-circular {
  margin: 3rem;
}
.purple-gradient {
  background-color: #1fd1f9;
  background-image: linear-gradient(to right, #5ce1e6, #cb6ce6, #ff66c4);
  transition: all 0.3s ease;
  color: white;
  transition: all 0.3s ease-out;
}
</style>
