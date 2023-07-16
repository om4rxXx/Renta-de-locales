<template>
  <v-row class="mx-4" style="height: 50px" justify="center" align="center">
    <v-col style="text-align: right" cols="12" sm="6" md="11">
      <h2>Marcus Obrien</h2>
    </v-col>
    <v-col cols="12" sm="6" md="1">
      <v-container fluid style="height: 100%">
        <v-menu
          bottom
          min-width="50px"
          rounded="xl"
          offset-y
          nudge-bottom="8"
          transition="slide-y-transition"
        >
          <template v-slot:activator="{ on }">
            <v-btn icon x-large v-on="on">
              <v-avatar class="profile" color="grey" size="60px">
                <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
              </v-avatar>
            </v-btn>
          </template>

          <v-card>
            <v-list-item-content class="justify-center">
              <div class="mx-auto text-center">
                <p class="text-caption mt-1">
                  {{ user.email }}
                </p>
                <v-divider class="my-3"></v-divider>

                <v-btn depressed rounded text @click="dialog = true">
                  Edit Account
                </v-btn>

                <v-divider class="my-3"></v-divider>
                <v-btn depressed rounded text to="/loin"> Disconnect </v-btn>
              </div>
            </v-list-item-content>
          </v-card>
        </v-menu>
        <v-dialog v-model="dialog" persistent width="800">
          <v-card class="rounded-xl">
            <v-card-text>
              <v-container>
                <v-row class="mt-5">
                  <v-col
                    cols="12"
                    sm="6"
                    md="4"
                    class="d-flex justify-center align-center"
                  >
                    <v-card flat class="d-flex justify-center">
                      <v-avatar size="150">
                        <img
                          src="https://cdn.vuetifyjs.com/images/john.jpg"
                          alt="John"
                        />
                      </v-avatar>

                      <v-btn color="#5CBBF6" disable fab dark absolute bottom>
                        <v-icon>mdi-pencil</v-icon>
                      </v-btn>
                    </v-card>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field
                      rounded
                      dense
                      label="Apellido Paterno"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="Apellido Materno"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="Teléfono"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="Dirección"
                      outlined
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field
                      rounded
                      dense
                      label="Nombre"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="Correo"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="Empresa"
                      outlined
                      color="primary"
                    ></v-text-field>
                    <v-text-field
                      rounded
                      dense
                      label="RFC"
                      outlined
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-row>
                    <v-row class="d-flex justify-end">
                      <v-col class="d-flex justify-space-around">
                        <v-btn
                          class="ml-2"
                          dark
                          rounded
                          color="#34A853"
                          @click="dialog = false"
                        >
                          Guardar
                        </v-btn>
                        <v-btn
                          dark
                          rounded
                          color="#FF5252"
                          @click="dialog = false"
                        >
                          Cancelar
                        </v-btn>
                      </v-col>
                      <v-col cols="12" sm="12" md="8">
                        <v-text-field
                          rounded
                          dense
                          label="Comentarios"
                          outlined
                          color="primary"
                        ></v-text-field>
                      </v-col>
                    </v-row>
                  </v-row>
                </v-row>
              </v-container>
            </v-card-text>

            <v-card-actions class="d-flex justify-start"> </v-card-actions>
          </v-card>
        </v-dialog>
      </v-container>
    </v-col>
  </v-row>
</template>

<script>
import Nav from "../components/Nav.vue";

export default {
  data: () => ({
    reveal: false,
    dialog: false,
    dialog1: false,

    user: {
      image: "https://avatars0.githubusercontent.com/u/9064066?v=4&s=460",
      fullName: "John Doe",
      email: "john.doe@doe.com",
    },
  }),
};
</script>