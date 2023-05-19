<template>
  <v-app>
    <Nav></Nav>
    <main>
      <v-main>
        <div class="d-flex justify-start mt-15 ml-10">
          <h1>Contratos</h1>
        </div>
        <v-row class="d-flex justify-start mt-10 mx-4">
          <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
            <v-list class="mt-0 pt-0"
              ><v-list-item class="d-flex justify-center">
                <v-list-item-icon>
                  <v-dialog
                    v-model="dialog1"
                    persistent
                    max-width="400"
                    class="rounded-xl"
                  >
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn color="red" icon dark v-bind="attrs" v-on="on">
                        <v-icon color="red">mdi-trash-can-outline</v-icon>
                      </v-btn>
                    </template>
                    <v-card class="rounded-xl">
                      <v-card-title class="text-h5">
                        Esta seuro que desea eliminar el contrato?
                      </v-card-title>
                      <v-card-text class="d-flex justify-center">
                        <v-icon large color="yellow accent-3">
                          mdi-alert
                        </v-icon></v-card-text
                      >
                      <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn
                          color="yellow accent-4"
                          text
                          @click="dialog1 = false"
                        >
                          Eliminar
                        </v-btn>
                        <v-btn
                          color="yellow accent-4"
                          text
                          @click="dialog1 = false"
                        >
                          Cancelar
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-dialog>
                </v-list-item-icon>

                <v-list-item-content class="d-flex justify-center">
                  <div class="d-flex justify-center">
                    <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                  </div>
                </v-list-item-content>
                <v-list-item-icon>
                  <v-btn color="#5CBBF6" icon>
                    <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                  </v-btn>
                </v-list-item-icon>
              </v-list-item>
              <v-list-item class="d-flex justify-center">
                <v-btn class="ma-2" icon fab absolute color="black">
                  <v-icon x-large>mdi-file-sign</v-icon>
                </v-btn></v-list-item
              >
            </v-list>

            <v-card-text>
              <div class="my-1 font-weight-black">Nombre: inovva sport</div>
              <div class="my-1 font-weight-black">Tipo: Contratozo</div>
              <div class="my-1 font-weight-black">
                Fecha de creación: 28/12/2018
              </div>
              <div class="my-1 font-weight-black">
                Fecha de inicio: 31/02/2019
              </div>
              <div class="my-1 font-weight-black">
                Fecha de Finalizacionación:31/02/2022
              </div>
              <div class="my-1 font-weight-black">Estatus: Nice</div>
            </v-card-text>
          </v-card>
        </v-row>

        <!--
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
      </v-row>-->
      </v-main>
    </main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    reveal: false,
    dialog: false,
    dialog1: false,
  }),
};
</script>

<style>
</style>