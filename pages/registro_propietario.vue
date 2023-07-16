<template>
  <v-app>
    <Nav></Nav>

    <v-main>
      <Header></Header>
      <v-row class="mx-4" justify="left">
        <v-col>
          <span class="text-h3">Registrar Propietario</span>
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
                      <h3 style="margin-bottom: 2%">Nombre</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="Nombre"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Apellido Paterno</h3>
                    </div>
                    <v-text-field
                      label="Apellido Paterno"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Apellido Materno</h3>
                    </div>
                    <v-text-field
                      label="Apellido Materno"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Correo Electrónico</h3>
                    </div>
                    <v-text-field
                      label="Correo Electrónico"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Teléfono</h3>
                    </div>
                    <v-text-field
                      label="Teléfono"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Dirección</h3>
                    </div>
                    <v-text-field
                      label="Dirección"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">RFC</h3>
                    </div>
                    <v-text-field
                      rounded
                      label="RFC"
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Tipo de Propietario</h3>
                    </div>
                    <v-text-field
                      label="Tipo de Propietario"
                      rounded
                      outlined
                      dense
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <div class="mx-auto text-left">
                      <h3 style="margin-bottom: 2%">Fotos</h3>
                    </div>
                    <v-file-input
                      rounded
                      label="Fotos"
                      outlined
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

