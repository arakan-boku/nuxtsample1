<template>
  <div>
    <div class="tile is-ancestor">
      <div class="tile content  is-parent is-vertical is-2">
        <article class="tile is-child box">
          <NLink to="/about">
            <h3>{{ linkname1 }}</h3>
          </NLink>
          <div class="block">
            <b-icon pack="fas" icon="tachometer-alt" size="is-large" type="is-primary" />
            <span class="subtitle">速度計</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child  box">
          <NLink to="/cityapi">
            <h3>{{ linkname2 }}</h3>
          </NLink>
          <div class="block">
            <b-icon pack="fas" icon="tty" size="is-large" type="is-primary" />
            <span class="subtitle">電話</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child box">
          <NLink to="/awesome">
            <h3>{{ linkname4 }}</h3>
          </NLink>
          <div class="block">
            <b-icon pack="fas" icon="angry" size="is-large" type="is-primary" />
            <span class="subtitle">怒り顔</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child box">
          <NLink to="/vxdemo">
            <h3>{{ linkname5 }}</h3>
          </NLink>
          <div class="block">
            <b-icon pack="fas" icon="anchor" size="is-large" type="is-primary" />
            <span class="subtitle">イカリ</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2" />
    </div>
    <div class="tile is-ancestor">
      <div class="tile content is-parent is-vertical is-2" />
      <div class="tile content  is-parent is-vertical is-2">
        <article class="tile is-child box">
          <a :href="outurl">
            <h3>{{ linkname3 }}</h3>
          </a>
          <div class="block">
            <b-icon pack="fas" icon="crow" size="is-large" type="is-primary" />
            <span class="subtitle">カラス</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child  box">
          <p class="title">
            Icon6
          </p>
          <div class="block">
            <b-icon pack="fas" icon="box-open" size="is-large" type="is-primary" />
            <span class="subtitle">開く箱</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child box">
          <p class="title">
            Icon7
          </p>
          <div class="block">
            <b-icon pack="fas" icon="chess" size="is-large" type="is-primary" />
            <span class="subtitle">チェス</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2">
        <article class="tile is-child box">
          <p class="title">
            Icon8
          </p>
          <div class="block">
            <b-icon pack="fas" icon="cloud" size="is-large" type="is-primary" />
            <span class="subtitle">クラウド</span>
          </div>
        </article>
      </div>
      <div class="tile content is-parent is-vertical is-2" />
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
      linkname5: '状態管理',
      linkname4: 'WEBフォント',
      linkname3: '外部リンク',
      linkname2: '市区町村',
      linkname1: '郵便番号'
    }
  },
  computed: {
    today () {
      return moment().format('YYYY/MM/DD dddd')
    }
  }
}
</script>
