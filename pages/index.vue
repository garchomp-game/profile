<template lang='pug'>
v-layout(column='', justify-center='', align-center='')
  v-flex(xs12='', sm8='', md6='')
    .text-center
    v-card.pt-6
      v-img.mx-auto(:src='dragonneImg' aspect-ratio='2' width='250')
      v-card-title.headline ようこそ！たくの自己紹介ページへ！
      v-card-text
        p 初めまして！たくです！
        p 現在は界隈に入ってからまだ日が浅いので、簡単な#[b 自己紹介サイト]でも作ろうかなと思い作ってみました！多分いろいろ改修していくかもですw
        p 現在は飲食をやっておりますが、実は元々ウェブ系のエンジニアをやっておりました。
        p スキルとしてはペーペーですが、せっかくなので活用できるところがあったら活用していきたいなとはどこかで思っています（叶わぬ願いか…？）
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
</style>