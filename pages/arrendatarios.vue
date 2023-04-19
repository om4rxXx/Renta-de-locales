<template>
  <v-app>
    <Nav></Nav>
    <main>
      <v-main>
        <div class="d-flex justify-start mt-15 ml-10">
          <h1>Arrendatarios</h1>
        </div>
        <v-row class="d-flex justify-start mt-10 mx-4">
          <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
            <v-list class="mt-0 pt-0"
              ><v-list-item class="d-flex justify-center">
                <v-list-item-icon>
                  <v-btn icon color="red">
                    <v-icon color="red">mdi-trash-can-outline</v-icon>
                  </v-btn>
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
                <v-avatar size="62">
                  <img
                    src="https://cdn.vuetifyjs.com/images/john.jpg"
                    alt="John"
                  /> </v-avatar
              ></v-list-item>
            </v-list>

            <v-card-text>
              <div class="my-1 font-weight-black d-flex justify-center">
                Martha Samaniego Perez
              </div>
              <div class="my-1 font-weight-black d-flex justify-center">
                Martha12@gmail.com
              </div>
              <div class="my-1 font-weight-black d-flex justify-center">
                492 586 4525
              </div>
              <div class="my-1 font-weight-black d-flex justify-center">
                <v-btn class="mx-2" color="#4CAF50" icon>
                  <v-icon color="#4CAF50">mdi-currency-usd</v-icon>
                </v-btn>
                <v-btn class="mx-2" color="#5CBBF6" icon>
                  <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
                </v-btn>
              </div>
              <div class="my-0">
                <v-card-actions>
                  <v-btn
                    text
                    color="deep-purple lighten-2"
                    @click="reveal = true"
                  >
                    Learn More
                  </v-btn>
                </v-card-actions>

                <v-expand-transition>
                  <v-card
                    v-if="reveal"
                    class="transition-fast-in-fast-out v-card--reveal rounded-xl"
                    style="height: 85%"
                    height="20"
                  >
                    <v-card-text class="pb-0">
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                    <v-card-actions class="pt-0">
                      <v-btn
                        text
                        color="deep-purple lighten-2"
                        @click="reveal = false"
                      >
                        Close
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-expand-transition>
              </div>
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
  }),
};
</script>

<style>
.v-card--reveal {
  bottom: 1;
  opacity: 1 !important;
  position: absolute;
  width: 90%;
}
</style>