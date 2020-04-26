<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="#43a047"
      dark
      shrink-on-scroll
      prominent
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-5"
      scroll-threshold="500"
    >

      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title> <strong>TranVehi</strong> </v-toolbar-title>

      <v-spacer></v-spacer>

    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-5"
      class="overflow-y-auto"
      max-height=""
    >
      <v-container style="height: 128px;"></v-container>
    </v-sheet>
  </v-card>
</template>

<style lang="css" scoped>
.v-app-bar {
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