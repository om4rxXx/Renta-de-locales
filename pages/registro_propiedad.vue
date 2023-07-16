<template>
  <v-app>
    <Nav></Nav>
    <v-main>
      <Header></Header>
      <v-row class="mx-4" justify="left">
        <v-col>
          <span class="text-h3">Registrar Propiedad</span>
        </v-col>
      </v-row>
      <v-row class="mx-auto text-center" style="width: 90%">
        <v-col>
          <v-card elevation="10" rounded="xl">
            <v-card-title> </v-card-title>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Propiedad</h3>
                    </div>
                    <v-text-field
                      label="Propiedad"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Tipo de propiedad</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Tipo de propiedad"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Descripción</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Descripción"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Ubicación</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Ubicación"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Costo $</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Costo $"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Anticipo mínimo</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Anticipo mínimo"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Meses mínimos</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Meses mínimos"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Fotos</h3>
                    </div>
                    <v-file-input
                      label="Fotos"
                      outlined
                      rounded
                      multiple
                      state
                      chips
                      hint
                      dense
                    ></v-file-input>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>

            <v-card-actions>
              <div class="mx-auto text-center">
                <v-btn
                  rounded
                  color="red"
                  dark
                  @click="dialog = false"
                  style="margin: 10px"
                >
                  <v-icon>mdi-close</v-icon>
                  Cancelar
                </v-btn>
              </div>
              <div class="mx-auto text-center">
                <v-btn
                  rounded
                  color="primary"
                  dark
                  @click="dialog = false"
                  style="margin: 10px"
                >
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
import Nav from "../components/Nav.vue";
import Header from "../components/Header.vue";

export default {
  data: () => ({
    user: {
      image: "https://avatars0.githubusercontent.com/u/9064066?v=4&s=460",
      fullName: "John Doe",
      email: "john.doe@doe.com",
    },
  }),
};
</script>
