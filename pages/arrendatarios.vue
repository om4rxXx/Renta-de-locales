<template>
  <v-app>
    <Nav></Nav>

    <v-main>
      <Header></Header>
      <div class="d-flex justify-start mt-15 ml-10">
        <h1>Arrendatarios</h1>
      </div>
      <v-row class="d-flex justify-start mt-10 mx-4">
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/john.png"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/2.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/5.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
        <v-card class="mx-4 my-2 mr-10 rounded-xl" width="280" height="325">
          <v-list class="mt-0 pt-0"
            ><v-list-item class="d-flex justify-center">
              <v-list-item-icon>
                <v-btn color="red" icon dark @click="dialog1 = true">
                  <v-icon color="red">mdi-trash-can-outline</v-icon>
                </v-btn>
              </v-list-item-icon>

              <v-list-item-content class="d-flex justify-center">
                <div class="d-flex justify-center">
                  <v-list-item-subtitle class="ml-1"> </v-list-item-subtitle>
                </div>
              </v-list-item-content>
              <v-list-item-icon>
                <v-btn color="#5CBBF6" icon @click="dialog = true">
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-avatar size="62">
                <img
                  src="https://cdn.vuetifyjs.com/images/lists/2.jpg"
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
              <v-btn
                class="mx-2"
                color="#5CBBF6"
                icon
                @click="dialogContrato = true"
              >
                <v-icon color="#5CBBF6">mdi-file-document-multiple</v-icon>
              </v-btn>
            </div>
            <div class="my-0">
              <v-card-actions>
                <v-menu
                  color="primary"
                  rounded="xl"
                  offset-y
                  nudge-bottom="5"
                  transition="slide-y-transition"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="my-0"
                      v-bind="attrs"
                      v-on="on"
                      text
                      color="deep-purple lighten-2"
                    >
                      Mas info
                    </v-btn>
                  </template>
                  <v-card width="220">
                    <v-card-text>
                      <p class="text-h4 text--primary">Info</p>
                      <p class="font-weight-black">Cinepolis</p>
                      <p class="font-weight-black">Calle del gato 128</p>
                      <p class="font-weight-black">RFC: XD</p>
                      <p class="font-weight-black">Comentarios:</p>
                    </v-card-text>
                  </v-card>
                </v-menu>
              </v-card-actions>

              <!-- <v-expand-transition>
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
                </v-expand-transition>!-->
            </div>
          </v-card-text>
        </v-card>
      </v-row>

      <!----Dialogs------->
      <v-dialog v-model="dialog1" persistent max-width="400" class="rounded-xl">
        <v-card class="rounded-xl">
          <v-card-title class="text-h5">
            Esta seuro que desea eliminar al usuario?
          </v-card-title>
          <v-card-text class="d-flex justify-center">
            <v-icon large color="yellow accent-3">
              mdi-alert
            </v-icon></v-card-text
          >
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="yellow accent-4" text @click="dialog1 = false">
              Eliminar
            </v-btn>
            <v-btn color="yellow accent-4" text @click="dialog1 = false">
              Cancelar
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
      <!--------------->
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
      <!---------------->
      <v-dialog v-model="dialogContrato" persistent width="900">
        <v-card elevation="10" rounded="xl">
          <v-card-title>
            <h1 style="margin: 20px">Contrato</h1>
            <v-divider></v-divider>
            <div class="mx-auto text-center">
              <v-btn
                rounded
                color="red"
                dark
                @click="dialogContrato = false"
                style="margin: 10px"
              >
                <v-icon>mdi-close</v-icon>
              </v-btn>
            </div>
          </v-card-title>

          <div justify="center" align="center">
            <img src="~/assets/image.png" alt="John" width="800" />
          </div>

          <div class="mx-auto text-center">
            <v-btn
              rounded
              color="red"
              dark
              @click="dialogContrato = false"
              style="margin: 10px"
            >
              <v-icon>mdi-close</v-icon>
              Cerrar
            </v-btn>
          </div>
        </v-card>
      </v-dialog>
    </v-main>
  </v-app>
</template>

<script >
import Nav from "~/components/Nav.vue";

export default {
  components: {
    Nav,
  },
  data: () => ({
    dialogContrato: false,
    reveal: false,
    dialog: false,
    dialog1: false,
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