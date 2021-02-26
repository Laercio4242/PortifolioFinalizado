<template>
  <section id="items">
    <v-parallax
      class="col-12"
      :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
      :src="require(`../assets/icons/habilidades.png`)"
    >
      <v-container fill-height class="col-12">
        <v-row class="mx-auto">
          <v-col v-for="(item, i) in items" :key="i">
            <div class="text-center" style="margin-left: -867px; margin-top: 240px;">
              <div class="display-3 font-weight-black mb-4">
                <img
                  class="img-logo" style="background: white;"
                  :src="require(`../assets/icons/${item.logo}`)"
                />
              </div>

              <div class="title font-weight-regular text-uppercase">
                {{ item.text }}
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>
  </section>
</template>

<style>
.img-logo {
  width: 70px;
}
</style>