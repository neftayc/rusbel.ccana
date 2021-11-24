<template>
  <v-app>
    <v-app-bar fixed app color="primary" class="white--text">
      <span class="text-h6 font-weight-bold" v-text="title"></span>
      <v-spacer />
      <v-btn
        v-for="(item, i) in items"
        :key="'menu' + i"
        text
        class="no-background-hover text-uppercase text-subtitle-2 white--text"
        :ripple="false"
        active-class="accent"
        :href="item.to"
      >
        <span>{{ item.title }}</span>
      </v-btn>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer class="primary justify-center">
      <v-btn
        text
        color="white"
        class="text-none text-caption"
        href="https://www.linkedin.com/in/neftali-ccana-a3a419a5/"
        target="_blank"
      >
        LinkedIn
      </v-btn>
      <v-btn
        text
        color="white"
        class="text-none text-caption"
        href="mailto:rusbel.ccana@gmail.com"
        target="_blank"
        >Email</v-btn
      >
      <v-btn
        text
        color="white"
        class="text-none text-caption"
        href="https://github.com/neftayc"
        target="_blank"
      >
        Github
      </v-btn>
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
          title: 'Nosotros',
          to: '#about',
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
      title: '@Rusbel Ccana',
    }
  },
}
</script>

<style lang="scss">
.no-background-hover {
  &:hover {
    color: #f2cf00 !important;
  }
  &::before {
    background-color: transparent !important;
  }
}
</style>
