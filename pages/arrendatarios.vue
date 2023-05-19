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
                        Esta seuro que desea eliminar al usuario?
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
                  <v-dialog v-model="dialog" persistent width="800">
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn color="#5CBBF6" icon v-bind="attrs" v-on="on">
                        <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                      </v-btn>
                    </template>
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

                                <v-btn
                                  color="#5CBBF6"
                                  disable
                                  fab
                                  dark
                                  absolute
                                  bottom
                                >
                                  <v-icon>mdi-pencil</v-icon>
                                </v-btn>
                              </v-card>
                            </v-col>
                            <v-col cols="12" sm="6" md="4">
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Apellido Paterno"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Apellido Materno"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Teléfono"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Dirección"
                                outlined
                                color="primary"
                              ></v-text-field>
                            </v-col>
                            <v-col cols="12" sm="6" md="4">
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Nombre"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Correo"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
                                label="Empresa"
                                outlined
                                color="primary"
                              ></v-text-field>
                              <v-text-field
                                rounded
                                dense
                                v-model="email"
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
                                    v-model="email"
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

                      <v-card-actions class="d-flex justify-start">
                      </v-card-actions>
                    </v-card>
                  </v-dialog>
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
                  <v-menu transition="scroll-y-transition" color="primary">
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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
                  <v-menu
                    class="my-14"
                    transition="scroll-y-transition"
                    color="primary"
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

<script lang="ts">
import Nav from "~/components/Nav.vue";

export default {
  components: {
    Nav,
  },
  data: () => ({
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