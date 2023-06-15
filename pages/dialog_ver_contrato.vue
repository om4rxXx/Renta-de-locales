<template>
  <v-app>
    <Nav></Nav>
    <v-main>
      <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="80%">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              Open Dialog
            </v-btn>
          </template>

          <v-card elevation="10" rounded="xl">
            <v-card-title>
              <h1 style="margin: 20px">Contrato</h1>
              <v-divider></v-divider>
              <div class="mx-auto text-center">
                <v-btn
                  rounded
                  color="red"
                  dark
                  @click="dialog = false"
                  style="margin: 10px"
                >
                  <v-icon>mdi-close</v-icon>
                </v-btn>
              </div>
            </v-card-title>

            <div justify="center" align="center">
              <img src="~/assets/image.png" alt="John" />
            </div>

            <div class="mx-auto text-center">
              <v-btn
                rounded
                color="red"
                dark
                @click="dialog = false"
                style="margin: 10px"
              >
                <v-icon>mdi-close</v-icon>
                Cerrar
              </v-btn>
            </div>
          </v-card>
        </v-dialog>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import Nav from "../components/Nav.vue";

export default {
  data: () => ({
    dialog: false,
  }),
};
</script>