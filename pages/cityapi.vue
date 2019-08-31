<template>
  <div>
    <NLink to="/">
      ルートのページへ戻ります
    </NLink>
    <br>
    <img src="/jamap.JPG" alt="image03">
    <div v-if=" prefecturesJson.message == null">
      <select v-model="prefecturesSelected" @change="updateMunicipalitiesJson({prefecturesSelected})">
        <option value="" />
        <option v-for="pOption in prefecturesJson.result" :key="pOption.id" :value="pOption.prefCode">
          {{ pOption.prefName }}
        </option>
      </select>
    </div>
    <div v-if="municipalitiesJson != null">
      <div v-if="municipalitiesJson.message == null">
        <select v-model="municipalitiesSelected">
          <option v-for="mOption in municipalitiesJson.result" :key="mOption.id" :value="mOption.cityCode">
            {{ mOption.cityName }}
          </option>
        </select>
      </div>
    </div>
    <div v-else>
      <select v-model="municipalitiesSelected">
        <option value="" />
      </select>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      prefecturesSelected: '',
      municipalitiesSelected: '',
      municipalitiesJson: null
    }
  },
  async asyncData (context) {
    return { prefecturesJson: await context.app.$getPrefecturesJson() }
  },
  methods: {
    async updateMunicipalitiesJson ({ prefecturesSelected }) {
      this.municipalitiesJson = await this.$getmunicipalitiesJson(prefecturesSelected)
    }
  },
  head: {
    title: 'CityApi page'
  }
}
</script>
