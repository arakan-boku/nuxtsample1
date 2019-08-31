<template>
  <div>
    <div class="container content has-text-centered">
      <img src="~assets/00_nuxt.JPG" alt="image01">
    </div>
    <div class="container content has-text-centered">
      <NLink to="/about">
        <h3>{{ linkname1 }}</h3>
      </NLink>
    </div>
    <div class="container content has-text-centered">
      <NLink to="/cityapi">
        <h3>{{ linkname2 }}</h3>
      </NLink>
    </div>
    <div class="container content has-text-centered">
      <NLink to="/awesome">
        <h3>{{ linkname4 }}</h3>
      </NLink>
    </div>
    <div class="container content has-text-centered">
      <NLink to="/vxdemo">
        <h3>{{ linkname5 }}</h3>
      </NLink>
    </div>
    <div class="container content has-text-centered">
      <a :href="outurl">
        <h3>{{ linkname3 }}</h3>
      </a>
    </div>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  head: {
    title: 'First page'
  },
  data () {
    return {
      outurl: 'https://ja.nuxtjs.org/',
      linkname5: '状態管理（vuex）サンプル',
      linkname4: 'WEBフォントサンプル',
      linkname3: '外部リンク（v-bind）サンプル',
      linkname2: '市区町村(Select）サンプル',
      linkname1: '郵便番号(click)サンプル'
    }
  },
  computed: {
    today () {
      return moment().format('YYYY/MM/DD dddd')
    }
  }
}
</script>
