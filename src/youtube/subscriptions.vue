<template lang="pug">
.container(v-show="isLoaded")
  .page.right.active
    h5 Subscriptions
    .row
      .col.s12(v-for="item in itens")
        .card.no-padding.flat.transparent
          .row
            .col.s12.m4
              a.wave
                img.empty-state(:src="item.image")
                .absolute.right.bottom.small-margin.black.white-text.small-text &nbsp;00:00:00&nbsp;
            .col.s12.m8
              h5.no-margin {{ item.title }}
              div 10k views
              .space
              div Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget ligula eu lectus lobortis condimentum. Aliquam nonummy auctor massa. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
</template>

<script>
import domain from "./domain";
export default {
  mixins: [domain],
};
</script>