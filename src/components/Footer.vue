<template>
  <v-card class="mt-3">
    <v-footer v-bind="localAttrs" :padless="padless">
      <v-card flat tile width="100%" class="grey darken-4 text-center">
        <v-card-text>
          <v-tooltip bottom v-for="icon in icons" :key="icon.id">
            <template v-slot:activator="{ on }">
              <v-btn :to="icon.route" route dark class="mx-4" icon v-on="on">
                <v-icon size="32px">{{ icon.icon }}</v-icon>
              </v-btn>
            </template>
            <span>{{icon.tooltip}}</span>
          </v-tooltip>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} —
          <strong>KrakenBeast</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-card>
</template>



<script>
export default {
  methods: {
    switchMode: function() {
      this.$vuetify.theme.isDark = this.dark;
    }
  },
  data: () => ({
    icons: [
      { icon: "mdi-home", route: "/", tooltip: "INICIO" },
      { icon: "mdi-clipboard-text", route: "/sitekey", tooltip: "TRAMITES" },
      { icon: "mdi-ticket-account", route: "/movies", tooltip: "CONTACTANOS" },
      { icon: "mdi-google-maps", route: "/tvshows", tooltip: "UBICADOS" },
    ],
    padless: true,
    variant: "default"
  }),
  computed: {
    localAttrs() {
      const attrs = {};
      if (this.variant === "default") {
        attrs.absolute = false;
        attrs.fixed = false;
      } else {
        attrs[this.variant] = true;
      }
      return attrs;
    }
  }
};
</script> 
<style lang="css" scoped>
.v-card {
  background-image: linear-gradient(to right, #3a7bd5, #3a6073);
}
.theme--light.v-footer {
  padding: 0px;
}
.pop-close {
  position: absolute;
  right: 1px;
}
</style>


