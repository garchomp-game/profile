<template lang="pug">
    v-card.mx-auto(width='80%')
      v-card-title(primary-title='') たく（生身|背後)
      v-list(three-line='')
        template(v-for='(item, index) in items')
          v-divider(v-if='item.divider', :key='index', :inset='item.inset')
          v-list-item(v-else='', :key='item.title', @click='')
            v-list-item-content
              v-list-item-title(v-html='item.title')
              v-list-item-subtitle(v-html='item.subtitle')
      v-card-text
        .title.font-weight-bold 自己紹介
        p 改めましてこんにちは。たくです。和太鼓とケモノが大好きです。
        p 最近着ぐるみ界隈のことを知ったのでまだ手探り状態ではありますが、
          | 現在色々なイベントに行ってみたり、自作に挑戦してみたりしています（自作しんどすぎてつらい………
        p 今後人生初イベントだったkemocon12に何らかの形で恩返ししたいと思い、和太鼓企画を立ち上げることを検討しています。
        p 練習会のツイプラも５月か６月ごろから定期的に立てる予定です。日本の文化の一つである和太鼓をケモノたちと楽しめたらいいなと思っています…！
</template>

<script>

export default {
  data() {
    return {
      items: [
        {
          title: '名前',
          subtitle: 'たく'
        },
        {divider: true, inset: true,},
        {
          title: '性別',
          subtitle: 'オス'
        },
        {divider: true, inset: true,},
        {
          title: '種族',
          subtitle: '人間/バクフーン'
        },
        {divider: true, inset: true,},
      ]
    }
    },
}

</script>