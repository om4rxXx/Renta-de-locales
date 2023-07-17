<template>
  <v-app>
    <Nav />
    <v-main>
      <Header></Header>
      <v-row class="d-flex justify-space-center mt-15 ml-4">
        <v-col
          ><v-card class="mb-6 rounded-xl">
            <v-row>
              <v-avatar class="ma-10" size="160">
                <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
              </v-avatar>
              <div class="d-flex align-center">
                <v-list
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title> Marcus Obrien </v-list-item-title>
                    </v-list-item-content> </v-list-item
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-gmail</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title>
                        Marcus_Obrien@gmail.com
                      </v-list-item-title>
                    </v-list-item-content> </v-list-item
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-cellphone</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title> 4981191580 </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </div>
            </v-row>
            <v-btn
              color="#5CBBF6"
              class="mb-10"
              disable
              fab
              dark
              absolute
              bottom
              right
              @click="dialog = true"
            >
              <v-icon> mdi-pencil</v-icon>
            </v-btn></v-card
          >
          <v-row>
            <v-col>
              <v-card height="220" class="rounded-xl my-2">
                <div class="text-center">
                  <v-card-text>
                    <div class="mt-0 text-h6">Retribuciones</div>
                    <v-col>
                      <div class="d-flex justify-space-between my-5">
                        <div>Total de ingresos:</div>
                        <div>$89,000</div>
                      </div>
                      <div class="d-flex justify-space-between my-5">
                        <div>Total de manteniminetos:</div>
                        <div>$89,000</div>
                      </div>
                      <div
                        class="d-flex justify-space-between my-5 font-weight-black"
                      >
                        <div>Total neto:</div>
                        <div>$89,000</div>
                      </div>
                    </v-col>
                  </v-card-text>
                </div>
              </v-card>
            </v-col>
            <v-col>
              <v-card height="225" class="rounded-xl my-2">
                <div class="text-center">
                  <v-card-text>
                    <div class="mt-0 text-h6">Locales</div>
                    <div class="d-flex align-center">
                      <v-icon class="align-self-center" left color="success">
                        mdi-rectangle
                      </v-icon>
                      disponibles
                    </div>
                    <div class="d-flex align-center">
                      <v-icon
                        class="align-self-center"
                        left
                        color="grey lighten-1"
                      >
                        mdi-rectangle
                      </v-icon>
                      ocupados
                    </div>

                    <v-progress-circular
                      class="my-0 py-0"
                      :value="90"
                      :size="100"
                      :width="15"
                      color="success"
                    >
                      90%</v-progress-circular
                    >
                  </v-card-text>
                </div>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
        <v-col>
          <v-card class="rounded-xl mr-15" height="490">
            <v-row>
              <v-col>
                <v-card-title class="d-flex justify-center mb-0 pb-0"
                  >Semaforo de pagos</v-card-title
                >
                <v-data-table
                  :headers="headers"
                  :items="desserts"
                  hide-default-footer
                  height="420"
                  class="rounded-xl"
                >
                  <template v-slot:item.name="{ item }">
                    <v-avatar size="30" color="grey">
                      <v-img
                        src="https://cdn.vuetifyjs.com/images/john.jpg"
                      ></v-img>
                    </v-avatar>
                    {{ item.name }}
                  </template>

                  <template v-slot:item.calories="{ item }">
                    <v-chip :color="getColor(item.calories)" dark>
                      {{ item.carbs }}
                    </v-chip>
                  </template>

                  <template v-slot:item.fat>
                    <v-icon color="#25D366">mdi-whatsapp</v-icon>
                  </template>
                </v-data-table>
              </v-col></v-row
            ></v-card
          ></v-col
        >
      </v-row>
      <div class="d-flex justify-start mt-5 ml-10">
        <h1>Disponibles</h1>
      </div>
      <v-row class="d-flex justify-start mx-4">
        <v-col cols="3">
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/92/64/a1/9264a15a62b5b547cb72716c5f87051a.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="success"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                    to="/local"
                  >
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
              </v-card></template
            >
          </v-hover></v-col
        >
        <v-col cols="3">
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/7f/50/b0/7f50b0df1e8a5260e03ef119e0521f94.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="success"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                    to="/local"
                  >
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
              </v-card></template
            >
          </v-hover></v-col
        >
        <v-col cols="3">
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/1b/1a/37/1b1a37b490d81953e359d95455d882fe.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="success"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                    to="/local"
                  >
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
              </v-card></template
            >
          </v-hover></v-col
        >
        <v-col cols="3">
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/58/49/f1/5849f1c1c07200eff7aab4b58b2918b9.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="success"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                    to="/local"
                  >
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
              </v-card></template
            >
          </v-hover></v-col
        >
      </v-row>
      <div class="d-flex justify-start mt-5 ml-10">
        <h1>Ocupados</h1>
      </div>
      <v-row class="d-flex justify-start mx-4">
        <v-col cols="3"
          ><v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/c7/04/22/c70422c750792eba0785fae493d5ea68.jpg"
                  >
                  </v-img>

                  <v-btn
                    to="/local"
                    color="#FF5252"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                  >
                    <v-icon>mdi mdi-lock</v-icon>
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
              </v-card></template
            >
          </v-hover></v-col
        >
        <v-col cols="3"
          ><v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/736x/3b/f0/75/3bf0751d25c4f95f43982a22511efac6.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="#FF5252"
                    to="/local"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                  >
                    <v-icon>mdi mdi-lock</v-icon>
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
              </v-card></template
            >
          </v-hover></v-col
        >
        <v-col cols="3"
          ><v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/3c/0a/65/3c0a65c0f6c4f00b623fa5015469ac9b.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="#FF5252"
                    to="/local"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                  >
                    <v-icon>mdi mdi-lock</v-icon>
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
              </v-card></template
            >
          </v-hover></v-col
        ><v-col cols="3"
          ><v-hover>
            <template v-slot:default="{ hover }">
              <v-card
                :elevation="hover ? 24 : 6"
                class="my-2 mr-10 rounded-xl"
                height="300"
              >
                <v-card flat>
                  <v-img
                    height="150"
                    src="https://i.pinimg.com/564x/3c/0a/65/3c0a65c0f6c4f00b623fa5015469ac9b.jpg"
                  >
                  </v-img>

                  <v-btn
                    color="#FF5252"
                    to="/local"
                    disable
                    fab
                    dark
                    absolute
                    bottom
                    right
                  >
                    <v-icon>mdi mdi-lock</v-icon>
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
              </v-card></template
            >
          </v-hover></v-col
        >
      </v-row>
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
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Nav from "~/components/Nav.vue";
export default {
  components: {
    Nav,
  },
  data() {
    return {
      headers: [
        {
          text: "Nombre",
          align: "start",

          value: "name",
        },
        { text: "Status", value: "calories", sortable: false, align: "center" },
        { text: "Notificar", value: "fat", sortable: false, align: "center" },
      ],
      desserts: [
        {
          name: "Juan perez",
          calories: 500,
          fat: 6.0,
          carbs: "vencido",
        },
        {
          name: "Julion alvarez",
          calories: 237,
          fat: 9.0,
          carbs: "por vencer",
        },
        {
          name: "Eden Muñoz ",
          calories: 262,
          fat: 16.0,
          carbs: "por vencer",
        },
        {
          name: "Jan Carlos",
          calories: 305,
          fat: 3.7,
          carbs: "por vencer",
        },
        {
          name: "Natanael Cano",
          calories: 356,
          fat: 16.0,
          carbs: "por vencer",
        },
        {
          name: "Juanita pantoja",
          calories: 375,
          fat: 0.0,
          carbs: "por vencer",
        },
        {
          name: "Shakira",
          calories: 392,
          fat: 0.2,
          carbs: "por vencer",
        },
        {
          name: "Nicki nicol",
          calories: 408,
          fat: 3.2,
          carbs: "vencido",
        },
        {
          name: "Laila",
          calories: 452,
          fat: 25.0,
          carbs: "vencido",
        },
        {
          name: "KitKat",
          calories: 518,
          fat: 26.0,
          carbs: "vencido",
        },
      ],
      dialog: false,
    };
  },
  methods: {
    getColor(calories: number) {
      if (calories > 400) return "red";
      else if (calories < 400) return "orange";
      else return "green";
    },
  },
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

.v-progress-circular__background {
  stroke: red;
}
</style>
