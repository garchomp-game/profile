<template lang='pug'>
v-layout
  v-flex.text-center
    .mx-auto(width='80%')
      .display-2.my-3.font-weight-bold(primary-title='') 詳細ページ
      div
        p.font-weight-bold.font-italic ここでは自己紹介の詳細と、各キャラの紹介をしていきます！
    taku-profile.mt-5
    dragonne-profile.mt-5

</template>

<script>
import TakuProfile from '@/components/TakuProfile.vue';
import DragonneProfile from '@/components/DragonneProfile.vue';

export default {
  components: {
    TakuProfile,
    DragonneProfile
  },
}
</script>