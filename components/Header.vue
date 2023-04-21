<template>
     <v-row class="mx-4" style="height: 50px;"  justify="center" align="center">
        <v-col style="text-align: right;" cols="12" sm="6" md="11">
        <h2  >{{ user.fullName }}</h2>
        </v-col>
        <v-col cols="12" sm="6" md="1">
            <v-container fluid style="height: 100%; ">
            <v-menu bottom min-width="50px" rounded offset-y>
                <template v-slot:activator="{ on }">
                <v-btn icon x-large v-on="on">
                  <v-avatar size="50px">
                    <img v-if="user.image" alt="Avatar" src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                    <v-icon v-else :color="message.color" v-text="message.icon"></v-icon>
                  </v-avatar>
                </v-btn>
              </template>
              <v-card>
                <v-list-item-content class="justify-center">
                  <div class="mx-auto text-center">
                    <v-avatar size="50px">
                      <img v-if="user.image" alt="Avatar"
                        src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                      <v-icon v-else :color="message.color" v-text="message.icon"></v-icon>
                    </v-avatar>
                    <h3>{{ user.fullName }}</h3>
                    <p class="text-caption mt-1">
                      {{ user.email }}
                    </p>
                    <v-divider class="my-3"></v-divider>
                    <v-btn depressed rounded text>
                      Edit Account
                    </v-btn>
                    <v-divider class="my-3"></v-divider>
                    <v-btn depressed rounded text>
                      Disconnect
                    </v-btn>
                  </div>
                </v-list-item-content>
              </v-card>
            </v-menu>
            </v-container>
        </v-col>
      </v-row>
</template>

<script>
import Nav from "../components/Nav.vue";

export default {
  data: () => ({
    user: {
      image: 'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
      fullName: 'John Doe',
      email: 'john.doe@doe.com',
    },
  }),
}
</script>