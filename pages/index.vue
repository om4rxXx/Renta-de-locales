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
                <img src="~/assets/ALY.svg" alt="John" />
              </v-avatar>
              <div class="d-flex align-center">
                <v-list
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title> citas.Estetica </v-list-item-title>
                    </v-list-item-content> </v-list-item
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-gmail</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title> citas.Medicas </v-list-item-title>
                    </v-list-item-content> </v-list-item
                  ><v-list-item>
                    <v-list-item-icon>
                      <v-icon>mdi-cellphone</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                      <v-list-item-title> citas.Vacunacion </v-list-item-title>
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
                      {{ item.calories }}
                    </v-chip>
                  </template>
                  <template v-slot:item.fat>
                    <v-icon color="#25D366"> mdi-whatsapp </v-icon>
                  </template>
                </v-data-table></v-col
              ></v-row
            ></v-card
          ></v-col
        >
      </v-row>
      <div class="d-flex justify-start mt-5 ml-10">
        <h1>Dosponibles</h1>
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
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
        <h1>ocupados</h1>
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                  >
                  </v-img>

                  <v-btn color="#FF5252" disable fab dark absolute bottom right>
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                  >
                  </v-img>

                  <v-btn color="#FF5252" disable fab dark absolute bottom right>
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
                    src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                  >
                  </v-img>

                  <v-btn color="#FF5252" disable fab dark absolute bottom right>
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
          name: "Frozen Yogurt",
          calories: 500,
          fat: 6.0,
          carbs: "por vencer",
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
          fat: 9.0,
          carbs: "por vencer",
        },
        {
          name: "Eclair",
          calories: 262,
          fat: 16.0,
          carbs: "por vencer",
        },
        {
          name: "Cupcake",
          calories: 305,
          fat: 3.7,
          carbs: "por vencer",
        },
        {
          name: "Gingerbread",
          calories: 356,
          fat: 16.0,
          carbs: "por vencer",
        },
        {
          name: "Jelly bean",
          calories: 375,
          fat: 0.0,
          carbs: "por vencer",
        },
        {
          name: "Lollipop",
          calories: 392,
          fat: 0.2,
          carbs: "por vencer",
        },
        {
          name: "Honeycomb",
          calories: 408,
          fat: 3.2,
          carbs: "vencido",
        },
        {
          name: "Donut",
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
    };
  },
  methods: {
    getColor(calories: number) {
      if (calories > 400) return "red";
      else if (calories > 200) return "orange";
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
