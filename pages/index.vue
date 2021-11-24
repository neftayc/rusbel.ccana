<template>
  <div>
    <section id="about">
      <v-card
        tile
        flat
        height="70vh"
        class="transparent d-flex flex-column justify-center align-center"
      >
        <h1 class="text-h3 font-weight-bold mb-8">Desarrollador front-end</h1>
        <p class="text-h6 font-weight-light mb-12">
          Diseño y Codifico cosas maravillosas simples, y me encanta lo que
          hago.
        </p>
        <v-avatar size="210">
          <v-img :src="require('@/assets/avatar.jpeg')"></v-img>
        </v-avatar>
      </v-card>
      <v-img
        v-if="false"
        class="mx-auto"
        :src="require('@/assets/hero.svg')"
        width="600"
      ></v-img>
      <v-card
        height="90vh"
        class="primary white--text text-center pt-16"
        flat
        tile
      >
        <h2 class="text-h4 font-weight-bold pt-16 mb-8">
          Hola, soy Rusbel. Un placer conocerte.
        </h2>
        <p class="text-h6 font-weight-light mx-auto" style="max-width: 56%">
          Desde que comencé mi viaje como desarrollador frontend hace 5 años, he
          trabajado en la universidad donde estudie, he trabajado remotamente
          para startups y actualmente estoy colaborando con personas talentosas
          en la creación de productos digitales para el control de consumo de
          energia en los Centros de Datos. Soy tranquilo, seguro, naturalmente
          curioso y estoy trabajando constantemente en la mejora de mis
          habilidades, un bug a la vez.
        </p>
      </v-card>
      <v-container style="margin-top: -200px">
        <v-card color="white" light class="py-10 rounded-lg">
          <v-container>
            <v-row>
              <v-col class="text-center">
                <v-icon
                  class="text-h3 font-weight-light"
                  color="primary lighten-1"
                  >mdi-account-tie</v-icon
                >
                <v-avatar v-if="false" tile size="35" class="mb-6">
                  <v-img
                    contain
                    :src="require('@/assets/frontend.svg')"
                  ></v-img>
                </v-avatar>
                <h4 class="text-h6 font-weight-bold mb-3">Feature</h4>
                <p>
                  Me gusta codificar cosas desde cero y disfruto dando vida a
                  las ideas en el navegador.
                </p>
              </v-col>
              <v-divider vertical></v-divider>
              <v-col class="text-center">
                <v-icon
                  class="text-h3 font-weight-light"
                  color="primary lighten-1"
                  >mdi-certificate-outline</v-icon
                >
                <v-avatar v-if="false" tile size="35" class="mb-6">
                  <v-img
                    contain
                    :src="require('@/assets/designer.svg')"
                  ></v-img>
                </v-avatar>
                <h4 class="text-h6 font-weight-bold mb-3">Languages</h4>
                <p>
                  Vuejs, Angular, JavaScript, Nuxtjs, Vuetify, Vuex, Bootstrap
                </p>
              </v-col>
              <v-divider vertical></v-divider>
              <v-col class="text-center">
                <v-icon
                  class="text-h3 font-weight-light"
                  color="primary lighten-1"
                >
                  mdi-clipboard-text-multiple-outline
                </v-icon>
                <v-avatar v-if="false" tile size="35" class="mb-6">
                  <v-img contain :src="require('@/assets/mentor.svg')"></v-img>
                </v-avatar>
                <h4 class="text-h6 font-weight-bold mb-3">Dev Tools</h4>
                <p>
                  Github, Gitlab, Bitbucket, Visual Studio Code, Microsoft Team,
                  Slack, Notion, Asana, Miro, Codepen
                </p>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-container>
    </section>
    <section id="portafolio" class="py-16">
      <h2 class="text-h3 text-center font-weight-bold black--text mb-8">
        Portafolio
      </h2>
      <template v-for="(item, i) in portafolio">
        <v-container :key="'portafolio-item' + i" class="my-16">
          <v-row align="end">
            <v-col cols="12" sm="6">
              <v-img
                height="100%"
                contain
                :src="item.image"
                class="rounded-lg"
              ></v-img>
            </v-col>
            <v-col cols="12" offset-lg="1" sm="6" lg="5">
              <v-card flat tile light>
                <h3 class="text-h5 font-weight-bold mb-5">
                  {{ item.proyecto }}
                  <v-chip color="accent" outlined class="ml-2" label small>
                    {{ item.year }}
                  </v-chip>
                </h3>

                <p class="grey--text text-body-2 font-weight-light mb-6">
                  {{ item.description }}
                </p>
                <v-btn
                  depressed
                  class="
                    rounded-lg
                    text-none text-subtitle-2
                    font-weight-regular
                  "
                  color="primary"
                  :href="item.url"
                  target="_blank"
                  large
                  >Visitar sitio</v-btn
                >
              </v-card>
            </v-col>
          </v-row>
        </v-container>
        <v-divider :key="'portafolio-key' + i"></v-divider>
      </template>
    </section>
    <section id="contacts" class="py-16">
      <h2 class="text-h3 text-center font-weight-bold mb-8">Contactenos</h2>
      <v-container fluid>
        <v-row justify="center">
          <v-col cols="5">
            <v-form class="text-center">
              <v-text-field outlined label="EMAIL"></v-text-field>
              <v-textarea outlined label="MENSAJE"></v-textarea>
              <v-btn class="px-10" color="primary" depressed dark large
                >Enviar</v-btn
              >
            </v-form>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    portafolio: [
      {
        proyecto: 'ECoaaS - TycheTools',
        image: require('@/assets/portafolio/tychetools-ecoass.png'),
        description:
          'Una plataforma que muestra informes sobre la información recopilada en Centro de Datos. Permite tomar una mejor decision a los Directores y realizar acciones rapidas a los operadores de dicho Centro de Datos.',
        year: '2020 - 2021',
        url: 'https://tychetools.com/es/solutions/ecoaas',
      },
      {
        proyecto: 'TycheTools',
        image: require('@/assets/portafolio/Tychetools.png'),
        description:
          'Página web de la compania TycheTools, que ofrece herramientas perfectas para tomar mejores decisiones. Las soluciones innovadoras basadas en inteligencia artificial brindan información en tiempo real basada en datos sobre el consumo de energía, el comportamiento térmico, el flujo de aire y las anomalías.',
        year: '2020',
        url: 'https://tychetools.com/',
      },
      {
        proyecto: 'EasyMgt',
        image: require('@/assets/portafolio/easymgt-home.png'),
        description:
          'Una plataforma que permite revolucionar la información sobre las Propiedades para los Realtors, Property Management Co., HOA y Business Owners.',
        year: '2020',
        url: 'https://easy-mgt.com',
      },
    ],
  }),
}
</script>
