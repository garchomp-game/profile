<template lang='pug'>
v-layout
  v-flex.text-center
    v-card.mx-auto(width='80%')
      v-card-title(primary-title='') 詳細ページ
      v-card-text
        p ここでは自己紹介の詳細と、各キャラの紹介をしていきます！
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