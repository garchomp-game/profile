<template lang="pug">
    v-card.mx-auto(width='80%')
      v-card-title(primary-title='') ドラゴーネ
      v-list(three-line='')
        template(v-for='(item, index) in items')
          v-divider(v-if='item.divider', :key='index', :inset='item.inset')
          v-list-item(v-else='', :key='item.title', @click='')
            v-list-item-content
              v-list-item-title(v-html='item.title')
              v-list-item-subtitle(v-html='item.subtitle')
      v-card-text
        .title.font-weight-bold 自己紹介
        p ボクは仔竜のドラゴーネ！森で暮らしていたけど、とあるぽけもんという種族に拾われてここに来たんだ！
        p まだあまりニンゲンの世界のことはよくわからないけれども、みんな優しくてとても楽しく過ごしているがう〜
        p 好きなことはお散歩したり美味しいもの食べること！
        p 一応バトルもできるけど、あまり得意ではないガゥ………
        p みんなともたくさんおしゃべりしたいガゥ〜✨
</template>

<script>

export default {
  data() {
    return {
      items: [
        {
          title: '名前',
          subtitle: 'ドラゴーネ'
        },
        {divider: true, inset: true,},
        {
          title: '性別',
          subtitle: 'オス'
        },
        {divider: true, inset: true,},
        {
          title: '種族',
          subtitle: '仔竜'
        },
        {divider: true, inset: true,},
      ]
    }
  }
}

</script>