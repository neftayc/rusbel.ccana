<template>
  <div>
    <section id="home">
      <v-container style="height: 100vh">
        <v-row align="center" class="fill-height">
          <v-col cols="12" sm="9" md="7" lg="6">
            <v-card flat class="transparent px-4">
              <span class="text-h4 d-block mb-5">¡Hola! 👋 Soy</span>
              <h1
                class="
                  text-h3 text-sm-h2 text-md-h2 text-lg-h1
                  font-weight-bold
                  mb-5
                "
              >
                Neftali
                <br />
                Ccana Yucra
              </h1>
              <div class="text-h6 font-weight-bold accent--text mb-5">
                DEVELOPER FRONTEND <span class="text-h5">👩‍💻</span>
              </div>
              <p class="text-body font-weight-regular mb-8">
                Soy desarrollador front-end senior con sede en Cusco - Perú,
                siempre estoy resolviendo un bug a la vez.
              </p>

              <div>
                <v-btn
                  color="accent"
                  depressed
                  class="
                    rounded-xl
                    text-none
                    background--text
                    text-subtitle-1
                    font-weight-medium
                    mr-2
                    px-md-15
                  "
                  href="https://api.whatsapp.com/send?phone=+051901581092&text=Hola Neftali, espero poder hablar con usted sobre cómo dar vida a mis ideas."
                  target="_blank"
                  large
                >
                  Contáctame
                </v-btn>
                <v-btn
                  depressed
                  class="
                    text-none
                    rounded-xl
                    font-weight-light
                    text-subtitle-1
                    px-md-10
                  "
                  large
                  outlined
                  href="/neftali_ccana_cv.pdf"
                  download="Neftali Ccana Yucra CV"
                >
                  Descargar CV
                  <v-icon right>mdi-cloud-download</v-icon>
                </v-btn>
              </div>
            </v-card>
          </v-col>
          <v-col class="d-none d-sm-block" cols="12" sm="3" md="5" lg="6">
            <v-img :src="require('@/assets/stack.svg')"></v-img>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section id="about" class="primary-dark py-15">
      <v-container class="mt-15">
        <v-row justify="center" class="fill-height">
          <v-col
            cols="12"
            class="
              d-flex
              flex-column
              justify-center
              align-center
              d-md-none
              text-center
            "
          >
            <div>
              <div class="accent--text text-subtitle-2 d-flex align-center">
                Quien Soy
                <v-card
                  width="60px"
                  height="3px"
                  color="#0fb"
                  class="ml-3"
                ></v-card>
              </div>
              <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
                Acerca de mí
              </h2>
            </div>
          </v-col>
          <v-col cols="12" md="5">
            <v-card class="text-center transparent" flat tile>
              <v-avatar
                size="260"
                class="mx-auto mb-4 rounded-xl"
                tile
                style="box-shadow: 0 1.6rem 3.6rem rgb(2, 12, 27, 0.7)"
              >
                <v-img
                  :src="require('@/assets/avatar.jpg')"
                  position="bottom left"
                  style="opacity: 0.85"
                ></v-img>
              </v-avatar>
              <div class="text-h5 font-weight-bold">
                Rosbel Neftali Ccana Yucra
              </div>
              <div class="text-subtitle-2 text-uppercase accent--text">
                Ingeniero de Sistemas <br />
                <div class="text-none text-caption grey--text">
                  Desarrollador Front-end
                </div>
              </div>

              <v-card class="pa-2" color="transparent" outlined>
                <v-divider class="my-4"></v-divider>
                <v-row
                  v-for="(item, i) in [
                    { name: 'Nacionalidad', value: 'Peruano' },
                    { name: 'Ciudad', value: 'Cusco' },
                    { name: 'Email', value: 'rusbel.ccana@gmail.com' },
                    { name: 'Telefono', value: '+051 901581092' },
                  ]"
                  :key="'datos-' + i"
                  dense
                  class="text-left text-caption"
                >
                  <v-col cols="6" sm="5" md="4">{{ item.name }}:</v-col>
                  <v-col cols="6" sm="7" md="8" class="text-right"
                    ><span class="font-weight-light">{{
                      item.value
                    }}</span></v-col
                  >
                </v-row>
                <v-divider class="my-4"></v-divider>
              </v-card>
              <div class="d-flex justify-center">
                <v-btn
                  fab
                  small
                  outlined
                  class="mx-2"
                  href="https://github.com/neftayc"
                  target="_blank"
                >
                  <v-icon>mdi-github</v-icon>
                </v-btn>
                <v-btn
                  fab
                  small
                  outlined
                  class="mx-2"
                  href="https://www.linkedin.com/in/neftali-ccana-a3a419a5/"
                  target="_blank"
                >
                  <v-icon>mdi-linkedin</v-icon>
                </v-btn>
                <v-btn
                  fab
                  small
                  outlined
                  class="mx-2"
                  href="mailto:rusbel.ccana@gmail.com"
                  target="_blank"
                >
                  <v-icon>mdi-gmail</v-icon>
                </v-btn>
                <v-btn
                  fab
                  small
                  outlined
                  class="mx-2"
                  href="https://api.whatsapp.com/send?phone=+051901581092&text=Hola Neftali, espero poder hablar con usted sobre cómo dar vida a mis ideas."
                  target="_blank"
                >
                  <v-icon>mdi-phone-message</v-icon>
                </v-btn>
                <v-btn
                  fab
                  small
                  outlined
                  class="mx-2"
                  href="https://web.facebook.com/nefta.ccana"
                  target="_blank"
                >
                  <v-icon>mdi-facebook</v-icon>
                </v-btn>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" md="6" offset-md="1">
            <div class="mb-6 d-none d-md-block">
              <div
                class="accent--text text-subtitle-2 mb-3 d-flex align-center"
              >
                Quien Soy
                <v-card
                  width="60px"
                  height="3px"
                  color="#0fb"
                  class="ml-3"
                ></v-card>
              </div>
              <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
                Acerca de mí
              </h2>
            </div>
            <div class="text-center text-md-left">
              <div class="text-body-2 mb-15">
                <p>
                  ¡Hola! mi nombres es Neftali Ccana y disfruto construyendo
                  soluciones para la web. Desde que comencé mi viaje como
                  desarrollador frontend hace 5 años, he trabajado en la
                  universidad donde estudie, he trabajado remotamente para
                  startups y actualmente estoy colaborando con personas
                  talentosas en la creación de productos digitales para el
                  control de consumo de energia en los Centros de Datos.
                </p>
                <p>
                  Soy tranquilo, seguro, naturalmente curioso y estoy trabajando
                  constantemente en la mejora de mis habilidades, resolviendo un
                  bug a la vez.
                </p>
                <p>
                  Diseño y codifico cosas maravillosas, simples y me encanta lo
                  que hago.
                </p>
              </div>
              <v-btn
                depressed
                color="accent"
                class="
                  rounded-xl
                  text-none
                  background--text
                  text-subtitle-1
                  font-weight-medium
                  px-15
                "
                x-large
                href="/neftali_ccana_cv.pdf"
                download="Neftali Ccana Yucra CV"
              >
                Descargar CV
                <v-icon right>mdi-cloud-download</v-icon>
              </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section id="services" class="primary-dark pt-15">
      <v-container class="py-15">
        <div class="d-flex justify-center align-center flex-column mb-15">
          <div>
            <div class="accent--text text-subtitle-2 d-flex align-center">
              Lo que hago
              <v-card
                width="60px"
                height="3px"
                color="#0fb"
                class="ml-3"
              ></v-card>
            </div>
            <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
              Mis Habilidades
            </h2>
          </div>
          <p class="text-center text-caption text-md-body-1">
            Me gusta codificar desde cero y disfruto dando vida a las ideas en
            el navegador.
          </p>
        </div>
        <v-row>
          <v-col cols="12" sm="6" md="4">
            <v-card class="service-card interface">
              <v-card
                height="80"
                width="80"
                class="d-flex justify-center align-center mb-4"
                style="border-radius: 50%"
                color="rgb(65, 184, 131, 0.2)"
              >
                <img
                  height="42px"
                  width="auto"
                  class="rounded-0"
                  :src="require('@/assets/vue.png')"
                />
              </v-card>
              <h3 class="mb-6">Habilidades Técnicas</h3>
              <div>
                <div
                  v-for="(item, i) in [
                    { name: 'HTML Y CSS', value: '75' },
                    { name: 'JavaScript (ES6+)', value: '80' },
                    { name: 'Node.js', value: '50' },
                    { name: 'Vue.js', value: '90' },
                    { name: 'Nuxt', value: '90' },
                    { name: 'Vuetify', value: '90' },
                    { name: 'Vuex', value: '70' },
                  ]"
                  :key="'skill' + i"
                  class="mb-5"
                >
                  <div class="d-flex justify-space-between text-caption">
                    <h4 class="font-weight-regular">{{ item.name }}</h4>
                    <div class="grey--text font-weight-light">
                      {{ item.value }}%
                    </div>
                  </div>
                  <v-progress-linear
                    :value="item.value"
                    color="accent "
                  ></v-progress-linear>
                </div>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="4">
            <v-card class="service-card profesional">
              <v-card
                height="80"
                width="80"
                class="d-flex justify-center align-center mb-4"
                style="border-radius: 50%"
                color="rgba(227,31,113,.2)"
              >
                <img
                  height="42px"
                  width="auto"
                  class="rounded-0"
                  :src="require('@/assets/brackets.svg')"
                />
              </v-card>
              <h3 class="mb-6">Habilidades Profesionales</h3>
              <div>
                <div
                  v-for="(item, i) in [
                    { name: 'Comunicación y Liderazgo', value: '90' },
                    { name: 'Trabajo en equipo', value: '80' },
                    { name: 'Investigación y Creatividad', value: '95' },
                    { name: 'Dedicación', value: '90' },
                    { name: 'Gestión de Proyectos', value: '60' },
                    { name: 'Mejora Continua', value: '99' },
                    { name: 'Optimización de Procesos', value: '50' },
                  ]"
                  :key="'skill' + i"
                  class="mb-5"
                >
                  <div class="d-flex justify-space-between text-caption">
                    <h4 class="font-weight-regular">{{ item.name }}</h4>
                    <div>
                      <v-icon color="accent">mdi-check</v-icon>
                    </div>
                  </div>
                </div>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="4">
            <v-card class="service-card devs">
              <v-card
                height="80"
                width="80"
                class="d-flex justify-center align-center mb-4"
                style="border-radius: 50%"
                color="rgba(136,56,180,.2)"
              >
                <img
                  height="42px"
                  width="auto"
                  class="rounded-0"
                  :src="require('@/assets/devs.svg')"
                />
              </v-card>
              <h3 class="mb-6">Dev Tools</h3>
              <div>
                <div
                  v-for="(item, i) in [
                    { name: 'Github, Gitlab y Bitbucket', value: '90' },
                    { name: 'Visual Studio Code', value: '90' },
                    { name: 'Slack, Microsoft Team', value: '60' },
                    { name: 'Asana, Jira y Trello', value: '60' },
                    { name: 'Notion', value: '99' },
                    { name: 'Miro', value: '50' },
                    { name: 'Codepen', value: '50' },
                  ]"
                  :key="'skill' + i"
                  class="mb-5"
                >
                  <div class="d-flex justify-space-between text-caption">
                    <h4 class="font-weight-regular">{{ item.name }}</h4>
                    <div>
                      <v-icon color="accent">mdi-check</v-icon>
                    </div>
                  </div>
                </div>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="procesos py-15">
      <v-container>
        <div class="d-flex justify-center align-center flex-column mb-15">
          <div>
            <div class="accent--text text-subtitle-2 d-flex align-center">
              Flujo de Trabajo
              <v-card
                width="60px"
                height="3px"
                color="#0fb"
                class="ml-3"
              ></v-card>
            </div>
            <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
              Mi Proceso de Trabajo
            </h2>
          </div>
        </div>
        <v-row justify="center">
          <v-col
            v-for="(item, i) in [
              {
                icon: require('@/assets/work-idea.svg'),
                title: 'Descubrir',
                description:
                  'Realizo una investigación de usuarios para identificar el problema que quiero resolver.',
              },
              {
                icon: require('@/assets/work-plan.svg'),
                title: 'Definir',
                description:
                  'Pienso en posibles soluciones de diseño para el problema identificado.',
              },
              {
                icon: require('@/assets/work-sketch.svg'),
                title: 'Idear',
                description:
                  'Creo wireframes y bocetos del producto que estoy a punto de diseñar.',
              },
              {
                icon: require('@/assets/work-design.svg'),
                title: 'Prototipo',
                description:
                  'Creo diseño de alta fidelidad y prototipo de pantallas.',
              },
              {
                icon: require('@/assets/implement.svg'),
                title: 'Implemantar',
                description:
                  'Después de diseñar, lo entrego para su implementación.',
              },
            ]"
            :key="'proceso' + i"
          >
            <v-card
              class="pt-9 px-5 pb-3 fill-height rounded-lg service-card-process"
              color="primary"
              min-width="200"
            >
              <v-avatar size="24" tile class="mb-3">
                <img :src="item.icon" alt=""
              /></v-avatar>
              <h3 class="text-subtitle-1 font-weight-bold mb-2">
                {{ item.title }}
              </h3>
              <p class="text-body-2 mb-0">{{ item.description }}</p>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section id="portafolio" class="primary-dark pt-15">
      <div class="d-flex justify-center align-center flex-column mt-15 mb-10">
        <div>
          <div class="accent--text text-subtitle-2 d-flex align-center">
            Proyectos
            <v-card
              width="60px"
              height="3px"
              color="#0fb"
              flat
              class="ml-3"
            ></v-card>
          </div>
          <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
            Mi Portafolio
          </h2>
        </div>
      </div>
      <v-container>
        <template v-for="(item, i) in portafolio">
          <v-row
            :key="'portafolio-item' + i"
            :class="i % 2 ? 'text-left' : 'text-right'"
            align="center"
          >
            <v-col cols="12" :sm="5" :order="i % 2 ? 2 : 1">
              <v-img height="100%" :src="item.image" class="rounded-lg"></v-img>
            </v-col>
            <v-col cols="12" :sm="7" :order="i % 2 ? 1 : 2">
              <div class="mb-6">
                <v-chip color="accent" outlined label small>
                  {{ item.year }}
                </v-chip>
                <h3 class="text-h5 font-weight-bold">
                  {{ item.proyecto }}
                </h3>
              </div>
              <v-card
                light
                class="pa-4 rounded-lg mb-6 portafolio-card"
                color="primary"
                dark
              >
                <p class="text-body-1 font-weight-light" style="color: #a8b2d1">
                  {{ item.description }}
                </p>
              </v-card>
              <div class="mb-4">
                <span
                  v-for="dev in item.devtools"
                  :key="dev"
                  class="ml-3 text-body-2 font-weight-light"
                >
                  {{ dev }}
                </span>
              </div>
              <div>
                <v-btn
                  depressed
                  class="text-none text-subtitle-2 font-weight-regular"
                  color="accent "
                  :href="item.url"
                  target="_blank"
                  icon
                >
                  <v-icon>mdi-github</v-icon>
                </v-btn>
                <v-btn
                  depressed
                  class="text-none text-subtitle-2 font-weight-regular"
                  color="accent "
                  :href="item.url"
                  target="_blank"
                  icon
                >
                  <v-icon>mdi-open-in-new</v-icon>
                </v-btn>
              </div>
            </v-col>
          </v-row>
          <v-divider :key="'divider' + i" class="mt-6 mb-7"></v-divider>
        </template>
      </v-container>
    </section>
    <section id="contacts" class="primary-dark py-16">
      <div class="d-flex justify-center align-center flex-column mt-15 mb-10">
        <div>
          <div class="accent--text text-subtitle-2 d-flex align-center">
            Contácteme
            <v-card
              width="60px"
              height="3px"
              color="#0fb"
              flat
              class="ml-3"
            ></v-card>
          </div>
          <h2 class="text-h5 text-lg-h4 font-weight-bold mb-2">
            Ponerse en contacto
          </h2>
        </div>
        <p class="text-caption text-md-body-1">
          Estoy disponible para trabajar en sus proyectos y dar vida a sus
          ideas. Estoy a solo un clic de distancia.
        </p>
      </div>
      <v-container class="mb-15">
        <v-row justify="center">
          <v-col cols="12">
            <div class="d-flex justify-center flex-wrap">
              <div
                v-for="(item, i) in [
                  { icon: 'mdi-pin', text: 'Cusco, Perú' },
                  { icon: 'mdi-email', text: 'rusbel.ccana@gmail.com' },
                  { icon: 'mdi-phone', text: '+051 901581092' },
                  {
                    icon: 'mdi-linkedin',
                    text: 'linkedin.com/in/neftali-ccana-a3a419a5',
                  },
                ]"
                :key="'contacto' + i"
                class="text-center mx-4 mb-6"
              >
                <v-avatar color="accent" size="38">
                  <v-icon color="primary-dark">{{ item.icon }}</v-icon>
                </v-avatar>
                <v-list-item-title class="text-caption text-md-body-1">{{
                  item.text
                }}</v-list-item-title>
              </div>
            </div>
          </v-col>
          <v-col v-if="false" cols="12" md="7">
            <v-form class="text-center">
              <v-text-field outlined label="Nombre"></v-text-field>
              <v-text-field outlined label="Email"></v-text-field>
              <v-textarea outlined label="Ingrese su Mensaje"></v-textarea>
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
        image: require('@/assets/portafolio/2.png'),
        description:
          'Una plataforma que muestra informes sobre los datos recopilados en los Centro de Datos. Permitiendo tomar una mejor decision a los Directores y realizar acciones rapidas a los operadores de dicho Centro de Datos.',
        year: '2020 - 2021',
        url: 'https://tychetools.com/es/solutions/ecoaas',
        devtools: ['Vue.js', 'Nuxt', 'Vuetify', 'Vuex', 'Axios', 'Django'],
      },
      {
        proyecto: 'TycheTools',
        image: require('@/assets/portafolio/1.png'),
        description:
          'Página web de la compania TycheTools, que ofrece herramientas perfectas para tomar mejores decisiones. Las soluciones innovadoras basadas en inteligencia artificial brindan información en tiempo real basada en datos sobre el consumo de energía, el comportamiento térmico, el flujo de aire y las anomalías detectadas en los Centro de Datos.',
        year: '2020',
        url: 'https://tychetools.com/',
        devtools: ['Vue.js', 'Nuxt', 'Vuetify'],
      },
      {
        proyecto: 'EasyMgt',
        image: require('@/assets/portafolio/easymgt-home.png'),
        description:
          'Una plataforma que permite revolucionar la información sobre las Propiedades para los Realtors, Property Management Co., HOA y Business Owners.',
        year: '2020',
        url: 'https://easy-mgt.com',
        devtools: ['Vue.js', 'Nuxt', 'Vuetify', 'Vuex', 'Axios', 'Django'],
      },
    ],
  }),
}
</script>
<style lang="scss" scoped>
.procesos {
  position: relative;
  z-index: 1;
  &::after {
    content: '';
    background: linear-gradient(
        to right bottom,
        rgba(2, 12, 27, 0.9),
        rgba(2, 12, 27, 1)
      ),
      url('~/assets/bg.jpeg') no-repeat center center;
    background-size: cover;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: -1;

    // gradient="to right bottom, rgba(2, 12, 27, .9), rgba(2, 12, 27, 1)"
  }
}
.service-card {
  background: var(--v-primary-base);
  box-shadow: 0 10px 30px -15px rgba(2, 12, 27, 0.7);
  // box-shadow: 0 1.6rem 2.4rem rgb(0, 0, 0, 0.25);
  border-radius: 0.8rem;
  width: 35.7rem;
  min-height: 300px;
  max-width: 100%;
  padding: 1.6rem 4.3rem 2.2rem 3.5rem;
  position: relative;
  &.interface::after {
    background: rgb(65, 184, 131);
  }
  &.profesional::after {
    background: #e31f71;
  }
  &.devs::after {
    background: #8838b4;
  }
  &::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 1rem;
    bottom: 0;
    left: 0;
    border-radius: 0 0 0.8rem 0.8rem;
  }
}
.service-card-process {
  box-shadow: 0 1.6rem 3.6rem rgba(2, 12, 27, 0.7) !important;
  cursor: pointer;
}
.portafolio-card {
  box-shadow: 0 10px 30px -15px rgba(2, 12, 27, 0.7);
  position: relative;
  z-index: 2;
  padding: 25px;
}
</style>
