

<template>
  <v-app>
    <Nav></Nav>
    <v-main>
      <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="70%">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" dark v-bind="attrs" v-on="on">
              Open Dialog
            </v-btn>
          </template>

          <v-card elevation='10' rounded='xl'>
            <v-card-title>
              <h1 style="margin: 20px;">Editar Arrentadatrio</h1>
            </v-card-title>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols="2" sm="6" md="4" align="center">
                    <v-row>
                      <v-col cols="1" sm="6" md="12" align="center">
                        <v-avatar size="200px">
                          <v-img v-if="user.image" alt="Avatar"
                            src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460">
                          </v-img>
                         </v-avatar>
                      </v-col>
                      <v-col cols="1" sm="6" md="12">
                        <v-btn color="primary" fab large dark :loading="isSelecting" @click="onButtonClick">
                          <v-icon>mdi-pencil</v-icon>
                        </v-btn>
                        <input ref="uploader" class="d-none" type="file" accept="image/*" @change="onFileChanged">
                      </v-col>
                      <v-col cols="1" sm="6" md="12">
                      </v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12"></v-col>
                      <v-col cols="1" sm="6" md="12">
                        <v-card-actions>
                          <div class="mx-auto text_left">
                            <v-btn rounded color="red" dark @click="dialog = false" style="margin : 10px">
                              <v-icon>mdi-close</v-icon>
                              Cancelar
                            </v-btn>
                          </div>
                          <div class="mx-auto text-left">
                            <v-btn rounded color="primary" dark @click="dialog = false" style="margin : 10px ">
                              <v-icon>mdi-plus</v-icon>
                              Guardar
                            </v-btn>
                          </div>
                        </v-card-actions>
                      </v-col>
                    </v-row>
                  </v-col>
                  <v-col cols="2" sm="6" md="8" align="center">
                    <v-row>
                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Nombre completo</h3>
                        </div>
                        <v-text-field label="Nombre completo" outlined dense></v-text-field>
                      </v-col>
                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Dirección</h3>
                        </div>
                        <v-text-field label="Dirección" outlined dense> </v-text-field>
                      </v-col>

                      <v-col cols="12" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Teléfono</h3>
                        </div>
                        <v-text-field label="Teléfono" outlined dense></v-text-field>
                      </v-col>

                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Correo Electrónico</h3>
                        </div>
                        <v-text-field label="Correo Electrónico" outlined dense> </v-text-field>
                      </v-col>

                      <v-col cols="2" sm="6" md="6">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">RFC</h3>
                        </div>
                        <v-text-field label="RFC" outlined dense> </v-text-field>
                      </v-col>
                      <v-col cols="12" sm="12" md="12">
                        <div class="mx-auto text-left">
                          <h3 style="margin-bottom: 2%;">Comentarios</h3>
                        </div>
                        <v-text-field label="Comentarios" outlined dense> </v-text-field>
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>

          </v-card>
        </v-dialog>
      </v-row>
    </v-main>
  </v-app>
</template>


<script>
import Nav from "../components/Nav.vue";

export default {
  data: () => ({
    dialog: false,
    user: {
      image: 'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
      fullName: 'John Doe',
      email: 'john.doe@doe.com',
    },
    selectedFile: null,
    isSelecting: false
  }),
  computed: {
    buttonText() {
      return this.selectedFile
        ? this.selectedFile.name
        : this.defaultButtonText;
    }
  },
  methods: {
    onButtonClick() {
      this.isSelecting = true;
      window.addEventListener(
        "focus",
        () => {
          this.isSelecting = false;
        },
        { once: true }
      );

      this.$refs.uploader.click();
    },
    onFileChanged(e) {
      this.selectedFile = e.target.files[0];

      // do something
    }
  }
}
</script>

