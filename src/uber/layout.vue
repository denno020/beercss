<template lang="pug">
div
  themes(v-model="$data")
    .large-space
    .medium-space

  #layout

  .menu.top.black
    .row.no-wrap.middle-align
      .col
        nav.padding
          a
            img(height="21", :src="'/uber-dark.png'")
          button.small-padding.wave.light.none.white-text.capitalize.m.l.large-text(
            data-ui="#dropdown-ride"
          ) 
            span Ride
            #dropdown-ride.dropdown.no-wrap(data-ui="#dropdown-ride")
              a Overview
              a Price calculator
              a Cities
              a Companies
              .divider
              a How it works
              a Safety
              a Airports
          button.small-padding.wave.light.none.white-text.capitalize.m.l.large-text(
            data-ui="#dropdown-drive"
          ) 
            span Drive
            #dropdown-drive.dropdown.no-wrap(data-ui="#dropdown-drive")
              a Overview
              a Partner app
              a Safe
              a How to drive in your city
              a Make deliveries
              .divider
              a Requirements
              a Vehicle solutions
              a Safety
          button.small-padding.wave.light.none.white-text.capitalize.m.l.large-text(
            data-ui="#dropdown-more"
          ) 
            span More
            #dropdown-more.dropdown.no-wrap(data-ui="#dropdown-more")
              a Uber Eats
              a Make deliveries
              a Uber Health
              .divider
              a Uber for companies
              a Uber Freight
      .col
        nav.right-align
          button.small-padding.wave.light.none.white-text(data-ui="#themes")
            i.white-text brightness_medium
          a(href="/")
            img.circle(:src="'/favicon.png'")
</template>

<script>
import themes from "../shared/themes.vue";
import data from "../shared/data";

export default {
  components: {
    themes
  },
  data() {
    return data()
  },
  mounted() {
    this.isDark = /dark/.test(document.body.getAttribute("style"));
    ui();
  }
};
</script>

<style>
</style>