<template lang='pug'>
v-layout(column='', justify-center='', align-center='')
  v-flex(xs12='', sm8='', md6='')
    .text-center
    v-card.pt-6
      v-img.mx-auto(:src='dragonneImg' aspect-ratio='2' width='250')
      v-card-title.headline ようこそ！たくの自己紹介ページへ！
      v-card-text
        top-profile
      v-card-actions
        v-spacer
        v-btn(color='primary', nuxt='', to='/inspire') 自己紹介詳細ページへ
</template>

<script>
import Dragonne from '~/assets/images/dragonne.jpg'
import TopProfile from '~/components/TopProfile.vue'

export default {
  data () {
    return {
      dragonneImg: Dragonne
    }
  },
  components: {
    TopProfile
  }
}
</script>

<style lang="sass">
</style>