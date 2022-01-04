<template>
  <v-app>
    <v-app-bar
      fixed
      app
      color="rgb(2, 12, 27, 0.9)"
      class="white--text"
      height="90"
      elevation="0"
    >
      <v-container class="d-flex">
        <span class="text-h4 font-weight-bold" v-text="title"></span>
        <v-spacer />
        <v-btn
          v-for="(item, i) in items"
          :key="'menu' + i"
          text
          class="no-background-hover text-none text-subtitle-2 white--text"
          :ripple="false"
          active-class="secondary--text"
          :to="item.to"
          exact-active-class="secondary--text"
        >
          <span>{{ item.title }}</span>
        </v-btn>
      </v-container>
    </v-app-bar>

    <v-main>
      <Nuxt />
    </v-main>
    <v-footer class="background justify-center py-10">
      <div class="text-center">
        <div class="d-flex justify-center mb-4">
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
        <div class="text-subtitle-2 grey--text">
          © Copyright 2021 <span class="accent--text">Neftali</span>, Todos los
          derechos reservados
        </div>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Inicio',
          to: '#',
        },
        {
          icon: 'mdi-apps',
          title: 'Acerca de',
          to: '#about',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Skills',
          to: '#services',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Portafolio',
          to: '#portafolio',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Contactenos',
          to: '#contacts',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '@Nefta',
    }
  },
}
</script>

<style lang="scss">
.no-background-hover {
  &:hover {
    color: var(--v-secondary-base) !important;
  }
  &::before {
    background-color: transparent !important;
  }
}
</style>
