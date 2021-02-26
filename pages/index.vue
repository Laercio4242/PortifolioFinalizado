<template>
  <v-app dark>
    <div>
      <v-app-bar
        align="baseline"
        class="col-12"
        color="black"
        height="100"
        fixed
        app
      >
        <v-row
        align="center"
          justify-lg="end"
          justify-sm="center"
          style="display: flex; flex-wrap: nowrap"
          class="col-12"
          sm="6"
          md="4"
        >
          <a class="hidden-sm-and-down ma-3" v-bind="size"  target="_blank" href="https://github.com/Laercio4242">
            <img class="svgI" src="@/assets/icons/github.png" alt="github" />
          </a>
          <v-btn
            v-bind="size"
            class="ma-3"
            target="_blank"
            color="white"

            @click="$vuetify.goTo('#my-skills')"
          >
            <span class="black--text text--darken-1 font-weight-bold">
              Habilidades
            </span>
          </v-btn>
          <v-btn
            v-bind="size"
            class="ma-3"
            color="white"
            @click="$vuetify.goTo('#my-projects')"
          >
            <span class="black--text text--darken-1 font-weight-bold">
              Projetos
            </span>
          </v-btn>
          <v-btn
            v-bind="size"
            download
            class="ma-3 text-decoration-none"
            color="white"
            href="https://drive.google.com/u/0/uc?id=1_HtXPlNcNAPqCyjxLc3NVt9zJRC-O_VG&export=download"
          >
            <span class="black--text text--darken-1 font-weight-bold">
              Download CV
            </span>
          </v-btn>
        </v-row>
      </v-app-bar>
      <v-divider />
      <v-main>
        <v-app>
          <section id="hero">
            <v-row no-gutters>
              <v-img
                :max-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
                src="https://image.freepik.com/fotos-gratis/fundo-abstrato-codigo-binario_1048-11344.jpg"
              >
                <v-theme-provider dark>
                  <v-container fill-height>
                    <v-row
                      align="center"
                      class="white--text mx-auto"
                      justify="center"
                    >
                      <v-col class="white--text text-center" cols="12" tag="h1">
                        <span
                          :class="[
                            $vuetify.breakpoint.smAndDown
                              ? 'display-1'
                              : 'display-2',
                          ]"
                          class="font-weight-light"
                        >
                          Bem Vindo ao 
                        </span>

                        <br />

                        <span
                          :class="[
                            $vuetify.breakpoint.smAndDown
                              ? 'display-3'
                              : 'display-4',
                          ]"
                          class="font-weight-black"
                        >
                          Meu Portifólio
                        </span>
                      </v-col>

                      <v-btn
                        v-bind="size"
                        class="align-self-end"
                        fab
                        large
                        outlined
                        @click="$vuetify.goTo('#about-me')"
                      >
                        <v-icon>mdi-chevron-double-down</v-icon>
                      </v-btn>
                    </v-row>
                  </v-container>
                </v-theme-provider>
              </v-img>
            </v-row>
          </section>
          <section id="about-me">
            <div class="py-12"></div>

            <v-container class="text-center">
              <v-responsive class="mx-auto mb-8" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <v-responsive
                class="mx-auto title font-weight-light mb-8"
                max-width="720"
              >
                <h2 class="display-2 font-weight-bold mb-3">
                  Eu sou Laercio Aparecido Pedroso
                </h2>

                <span
                  >Consultor de Soluções Digitais, apaixonado por tecnologia e por desenvolvimento 😊.</span
                >
                <p>
                 Com 4 anos de experiência em desenvolvimento em Java, Angular, JavaScript e Node.
                </p>
              </v-responsive>

              <v-avatar class="elevation-12 mb-12" size="128">
                <v-img
                  src="https://avatars.githubusercontent.com/u/47425532?s=400&u=5031706f61f2a1ddf5492d1f7c9f114c0d1b18e6&v=4.jpg"
                ></v-img>
              </v-avatar>

              <div></div>
              <v-btn
                class="ma-2"
                color="white"
                target="_blank"
                href="https://github.com/Laercio4242"
                large
              >
                <img src="@/assets/icons/github.png" alt="github" />
                <span class="grey--text text--darken-1 font-weight-bold">
                  Github
                </span>
              </v-btn>
              <v-btn
                class="ma-3"
                color="white"
                target="_blank"
                href="https://www.linkedin.com/in/laercio-aparecido/"
                large
              >
                <img src="@/assets/icons/linkedin.png" alt="linkedin" />

                <span class="ml-2 grey--text text--darken-1 font-weight-bold">
                  Linkedin
                </span>
              </v-btn>
            </v-container>

            <div class="py-12"></div>
          </section>
          <section class="black">
            <div class="py-12"></div>

            <v-container
              style="width: 100vw"
              id="my-skills"
              class="text-center black"
            >
              <h2 class="display-2 font-weight-bold mb-3">Habilidades</h2>

              <v-responsive class="mx-auto mb-12" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <Skills />
            </v-container>

            <div class="py-12"></div>
          </section>
          <section id="features">
            <div class="py-12"></div>
            <v-divider />
            <v-container id="my-projects" class="text-center">
              <h2 class="display-2 font-weight-bold mb-3">
                PROJETOS EM QUE ATUEI
              </h2>

              <v-responsive class="mx-auto mb-12" width="56">
                <v-divider class="mb-1"></v-divider>

                <v-divider></v-divider>
              </v-responsive>

              <Timeline />
            </v-container>

            <div class="py-12"></div>
          </section>
          <v-divider />
        </v-app>
      </v-main>

      <v-footer class="justify-center" color="#292929" height="40">
        <div
          class="subtitle font-weight-light grey--text text--lighten-1 text-center"
        >
          &copy; {{ new Date().getFullYear() }} — Laercio Aparecido Pedroso - Todos direitos reservados
        </div>
      </v-footer>
    </div>
  </v-app>
</template>

<script>
import Skills from "../components/skills.vue";
import Timeline from "../components/timeline.vue";
export default {
  components: { Timeline, Skills },
  data() {
    return {
      clipped: false,
      fixed: false,
      title: "",
    };
  },
  computed: {
    size() {
      const size = { xs: "x-small", sm: "small",}[
        this.$vuetify.breakpoint.name
      ];
      return size ? { [size]: true } : {};
    },
  },
};
</script>
<style scoped>
.svgI {
  background: whitesmoke;
  border-radius: 50%;
  width: 50px;
  cursor: pointer;
}
</style>