<template>
  <v-app>
    <Nav></Nav>

    <v-main>
      <Header></Header>
      <div class="d-flex justify-start mt-15 ml-10">
        <h1>Contratos</h1>
      </div>
      <v-row class="d-flex justify-start mt-10 mx-4">
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                @click="dialogContrato = true"
                color="black"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                @click="dialogContrato = true"
                class="ma-2"
                icon
                fab
                absolute
                color="black"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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

        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
        <v-card class="mx-4 my-2 mr-5 rounded-xl" width="300" height="310">
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
                <v-btn color="#5CBBF6" @click="dialogedit = true" icon>
                  <v-icon color="#5CBBF6">mdi-pencil</v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item>
            <v-list-item class="d-flex justify-center">
              <v-btn
                class="ma-2"
                icon
                fab
                absolute
                color="black"
                @click="dialogContrato = true"
              >
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
      <!------------------------->
      <v-dialog v-model="dialog1" persistent max-width="400" class="rounded-xl">
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
            <v-btn color="yellow accent-4" text @click="dialog1 = false">
              Eliminar
            </v-btn>
            <v-btn color="yellow accent-4" text @click="dialog1 = false">
              Cancelar
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
      <!-------------------------------->
      <v-dialog v-model="dialogedit" persistent max-width="80%">
        <v-card elevation="10" rounded="xl">
          <v-card-title>
            <h1 style="margin: 20px">Registrar Contrato</h1>
          </v-card-title>
          <v-card-text>
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Contrato</h3>
                  </div>
                  <v-text-field
                    rounded
                    label="Contrato"
                    outlined
                    dense
                  ></v-text-field>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Tipo de Contrato</h3>
                  </div>
                  <v-text-field
                    rounded
                    label="Tipo de Contrato"
                    outlined
                    dense
                  ></v-text-field>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Propiedad</h3>
                  </div>
                  <v-text-field
                    rounded
                    label="Propiedad"
                    outlined
                    dense
                  ></v-text-field>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Fecha del contrato</h3>
                  </div>

                  <v-menu
                    ref="menu"
                    v-model="menu"
                    rounded="xl"
                    :close-on-content-click="false"
                    :return-value.sync="date"
                    transition="scale-transition"
                    offset-y
                    min-width="auto"
                  >
                    <template v-slot:activator="{ on, attrs }">
                      <v-text-field
                        rounded
                        v-model="date"
                        label="Selecciona fecha de creación"
                        prepend-icon="mdi-calendar"
                        readonly
                        v-bind="attrs"
                        v-on="on"
                      ></v-text-field>
                    </template>
                    <v-date-picker rounded v-model="date" no-title scrollable>
                      <v-spacer></v-spacer>
                      <v-btn text color="primary" @click="menu = false">
                        Cancel
                      </v-btn>
                      <v-btn
                        text
                        color="primary"
                        @click="$refs.menu.save(date)"
                      >
                        OK
                      </v-btn>
                    </v-date-picker>
                  </v-menu>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Fecha de Inicio</h3>
                  </div>

                  <v-menu
                    ref="menu2"
                    rounded="xl"
                    v-model="menu2"
                    :close-on-content-click="false"
                    :return-value.sync="date2"
                    transition="scale-transition"
                    offset-y
                    min-width="auto"
                  >
                    <template v-slot:activator="{ on, attrs }">
                      <v-text-field
                        rounded
                        v-model="date2"
                        label="Selecciona fecha de inicio"
                        prepend-icon="mdi-calendar"
                        readonly
                        v-bind="attrs"
                        v-on="on"
                      ></v-text-field>
                    </template>
                    <v-date-picker v-model="date2" no-title scrollable>
                      <v-spacer></v-spacer>
                      <v-btn text color="primary" @click="menu2 = false">
                        Cancel
                      </v-btn>
                      <v-btn
                        text
                        color="primary"
                        @click="$refs.menu2.save(date2)"
                      >
                        OK
                      </v-btn>
                    </v-date-picker>
                  </v-menu>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Fecha de Finalización</h3>
                  </div>
                  <v-menu
                    ref="menu3"
                    rounded="xl"
                    v-model="menu3"
                    :close-on-content-click="false"
                    :return-value.sync="date3"
                    transition="scale-transition"
                    offset-y
                    min-width="auto"
                  >
                    <template v-slot:activator="{ on, attrs }">
                      <v-text-field
                        rounded
                        v-model="date3"
                        label="Selecciona fecha de fin"
                        prepend-icon="mdi-calendar"
                        readonly
                        v-bind="attrs"
                        v-on="on"
                      ></v-text-field>
                    </template>
                    <v-date-picker rounded v-model="date3" no-title scrollable>
                      <v-spacer></v-spacer>
                      <v-btn text color="primary" @click="menu3 = false">
                        Cancel
                      </v-btn>
                      <v-btn
                        text
                        color="primary"
                        @click="$refs.menu3.save(date3)"
                      >
                        OK
                      </v-btn>
                    </v-date-picker>
                  </v-menu>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Depósito</h3>
                  </div>
                  <v-text-field
                    rounded
                    label="Depósito"
                    outlined
                    dense
                  ></v-text-field>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Arrendatario</h3>
                  </div>
                  <v-text-field
                    rounded
                    label="Arrendatario"
                    outlined
                    dense
                  ></v-text-field>
                </v-col>
                <v-col cols="12" sm="6" md="4">
                  <div class="mx-auto text-left">
                    <h3 style="margin-bottom: 2%">Duración</h3>
                  </div>
                  <v-text-field rounded label="Duración" outlined dense>
                  </v-text-field>
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
                @click="dialogedit = false"
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
                @click="dialogedit = false"
                style="margin: 10px"
              >
                <v-icon>mdi-plus</v-icon>
                Guardar
              </v-btn>
            </div>
          </v-card-actions>
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
    reveal: false,
    dialogContrato: false,
    dialogedit: false,
    dialog: false,
    dialog1: false,
  }),
  dates: {
    date: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    date2: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    date3: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    menu: false,
    menu2: false,
    menu3: false,
  },
};
</script>

<style>
</style>