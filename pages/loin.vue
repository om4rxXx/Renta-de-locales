<template>
  <v-app
    ><v-content>
      <v-row class="d-flex justify-center no-scroll mt-5 pt-5">
        <v-col cols="4">
          <v-card
            elevation="14"
            rounded="200"
            class="mx-auto mt-14 pt-14 rounded-xl"
            color="white"
          >
            <v-card-text>
              <div>
                <p class="text-h4 text-color d-flex justify-center">
                  <v-avatar class="pa-10" size="160">
                    <img
                      src="https://cdn.vuetifyjs.com/images/cards/server-room.jpg"
                      alt="John"
                    />
                  </v-avatar>
                </p>

                <h1 class="py-5 d-flex justify-center">Iniciar Sesión</h1>
              </div>
              <div class="mx-15 px-2 mb-3 d-flex justify-center">
                <v-text-field
                  rounded
                  dense
                  label="E-mail"
                  outlined
                  color="primary"
                ></v-text-field>
              </div>
              <div class="mx-15 px-2 mb-3 d-flex justify-center">
                <v-text-field
                  rounded
                  dense
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  label="Contraseña"
                  @click:append="show1 = !show1"
                  outlined
                  color="primary"
                ></v-text-field>
              </div>

              <div class="d-flex justify-end">
                <a
                  href="https://www.leagueoflegends.com/es-mx/"
                  class="text-decoration-none mr-10 pr-10"
                  >¿Olvidaste la contraseña?
                </a>
              </div>
              <p></p>
              <div class="d-flex justify-center">
                <v-btn
                  min-width="200"
                  min-height="50"
                  class="mb-6 btn-gradient btn-center white--text"
                  depressed
                  color="#3D76F2"
                  :loading="loading"
                  rounded
                  to="/"
                >
                  Iniciar Sesión
                </v-btn>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-content>
    <v-footer height="70" app class="footer-gradient" padless>
      <v-col
        class="py-1 text-center white--text"
        style="font-family: 'League Spartan', sans-serif; font-weight: 500"
        cols="12"
      >
        {{ new Date().getFullYear() }} — Vuetify
      </v-col>
    </v-footer></v-app
  >
</template>

<script>
export default {
  data() {
    return {
      show1: false,

      password: "Password",
      rules: {
        required: (value) => !!value || "Required.",
        min: (v) => v.length >= 8 || "Min 8 characters",
        emailMatch: () => `The email and password you entered don't match`,
      },
    };
  },
};
</script>
<style>
.btn-gradient {
  background-color: #1fd1f9;
  background-image: linear-gradient(to right, #5ce1e6, #cb6ce6, #ff66c4);
  transition: all 0.3s ease;
  color: white;
  transition: all 0.3s ease-out;
}
.footer-gradient {
  background-color: #1fd1f9;
  background-image: linear-gradient(to right, #5ce1e6 0%, #cb6ce6, #ff66c4);
  background-size: 200% auto;
  color: white;
  transition: all 0.3s ease-out;
}
</style>
