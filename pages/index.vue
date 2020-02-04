<template lang='pug'>
v-layout(column='', justify-center='', align-center='')
  v-flex(xs12='', sm8='', md6='')
    .text-center
    v-card.top-profile-card
      v-img.dragonne-center(:src='dragonneImg' aspect-ratio='2' width='250')
      v-card-title.headline ようこそ！たくの自己紹介ページへ！
      v-card-text ここにいろいろ書いていくよ！
      v-card-actions
        v-spacer
        v-btn(color='primary', nuxt='', to='/inspire') 自己紹介詳細ページへ
</template>

<script>
import Dragonne from '~/assets/images/dragonne.jpg'

export default {
  data () {
    return {
      dragonneImg: Dragonne
    }
  }
}
</script>

<style lang="sass">
  .top-profile-card
    padding-top: 30px
  .dragonne-center
    margin: 0 auto
</style>