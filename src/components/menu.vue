<template>
  <div class="demo-comp">
    <button @click="onOpen">Выбрать город</button>
    <div class="chosen">Город: {{ selected }}</div>
    <vue-search-panel
      v-model="value"
      :fetch-suggestions="getSuggestions"
      @select="onSelect"
      ref="searchPanel"
    >
    </vue-search-panel>
  </div>
</template>



<script>
import VueSearchPanel from 'vue-search-panel'
const testData = [
  { key: 'Москва', value: 'Москва' },
  { key: 'Санкт-Петербург' , value: 'Санкт-Петербург' },
  { key: 'Казань', value: 'Казань' },
  { key: 'Лондон', value: 'Лондон' },
  { key: 'Берлин', value: 'Берлин' },
  { key: 'Сидней', value: 'Сидней' },
  { key: 'Мюнхен', value: 'Мюнхен' },
  { key: 'Париж', value: 'Париж' },
  { key: 'Токио', value: 'Токио' },
  { key: 'Пекин', value: 'Пекин' },
  { key: 'Нью-Йорк', value: 'Нью-Йорк' },
  { key: 'Сан-Франциско', value: 'Сан-Франциско' },
  { key: 'LA', value: 'LA' },
  { key: 'Рим', value: 'Рим' },
  { key: 'Милан', value: 'Милан' },
  { key: 'Канберра', value: 'Канберра' },
  { key: 'Бойнос-Айрес', value: 'Бойнос-Айрес' },
  { key: 'Мадрид', value: 'Мадрид' },
  { key: 'Барселона', value: 'Барселона' },
  { key: 'Мехико', value: 'Мехико' },


]

export default {
  name: 'DemoComp',
  data () {
    return {
      value: '',
      selected: ''
    }
  },
  methods: {
    onOpen () {
      this.$refs.searchPanel.show()
    },
    onSelect (item) {
      this.selected = item.value
    },
    getSuggestions (query, cb) {
      cb(query ? testData.filter(item => { return item.value.includes(query) }) : testData)
    }
  },
  components: { VueSearchPanel }
}
</script>



<style scoped>
.chosen{
color:white;
font-family:Verdana, Geneva, Tahoma, sans-serif;
}
.hea{
	max-width: 800px;
	margin: 0 auto;
	font-size: 20px;
	background-color:blue;
}
.li_2{
	
	
	display: grid;
	grid-template-columns: 6fr 1fr 1fr;
}
.li_2 li{
	margin: 10px;
}
.li_1{
	text-decoration: underline;
}

</style>