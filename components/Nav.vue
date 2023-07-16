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
      <v-list-item-group active-class="purple-gradient white--text">
        <v-list-item-title class="font-weight-bold">Inicio</v-list-item-title>
        <v-list-item
          href="/
        "
        >
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Dashboard</v-list-item-title>
        </v-list-item>
        <v-list-item-title class="font-weight-bold">Registro</v-list-item-title>
        <v-list-item href="/registro_propiedad">
          <v-list-item-icon>
            <v-icon>mdi-folder-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Propiedad</v-list-item-title
          >
        </v-list-item>
        <v-list-item href="/registro_arrendatario">
          <v-list-item-icon>
            <v-icon>mdi-account</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Arrendatario</v-list-item-title
          >
        </v-list-item>
        <v-list-item href="/registro_propietario">
          <v-list-item-icon>
            <v-icon>mdi-account</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Propietario</v-list-item-title
          >
        </v-list-item>
        <v-list-item-title class="font-weight-bold">Catálogo</v-list-item-title>
        <v-list-item href="/tabla_mantenimientos">
          <v-list-item-icon>
            <v-icon>mdi-hammer-wrench</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Mantenimiento</v-list-item-title
          >
        </v-list-item>
        <v-list-item href="/contratos">
          <v-list-item-icon>
            <v-icon>mdi-book</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Contrato</v-list-item-title
          >
        </v-list-item>

        <v-list-item-title class="font-weight-bold"
          >Información</v-list-item-title
        >
        <!-- <v-list-item href="........">
          <v-list-item-icon>
            <v-icon>mdi-account-group</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Usuario</v-list-item-title
          > 
        </v-list-item>-->
        <v-list-item href="/arrendatarios">
          <v-list-item-icon>
            <v-icon>mdi-account-box-multiple</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Arrendatarios</v-list-item-title
          >
        </v-list-item>
        <v-list-item href="/Propietarios">
          <v-list-item-icon>
            <v-icon>mdi-home-group</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="font-weight-bold"
            >Propietarios</v-list-item-title
          >
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <template v-slot:append>
      <div class="pa-2">
        <v-btn elevation="0" to="/loin" block color="white">
          Logout <v-icon dark right> mdi-logout </v-icon></v-btn
        >
      </div>
    </template>
  </v-navigation-drawer>
</template>

<script lang="ts">
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
