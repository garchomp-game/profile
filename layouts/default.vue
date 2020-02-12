<template lang='pug'>
v-app(dark='')
  v-navigation-drawer(
    v-model='drawer', 
    :mini-variant='miniVariant', 
    :clipped='clipped', 
    fixed='', 
    app=''
  )
    v-list
      v-list-item(v-for='(item, i) in items', :key='i', :to='item.to', router='', exact='')
        v-list-item-action
          v-icon {{ item.icon }}
        v-list-item-content
          v-list-item-title(v-text='item.title')
  v-app-bar(:clipped-left='clipped', fixed='', app='')
    v-app-bar-nav-icon(@click.stop='drawer = !drawer')
    v-toolbar-title.toolbar-title-hover(v-text='title' @click='jumpIndex')
    v-spacer
  v-content
    v-container
      nuxt
  v-footer(:fixed='fixed', app='')
    span © 2020

</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'ホーム',
          to: '/'
        },
        {
          icon: 'mdi-format-list-bulleted',
          title: '自己紹介詳細',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'たくの自己紹介サイト'
    }
  },
  methods: {
    jumpIndex() {
      this.$router.push('/')
    }
  },
}
</script>

<style lang="sass">
  .toolbar-title-hover:hover
    cursor: pointer
</style>