<template>
  <div id="app">
    <div class="mainn">
    <div class="hea">
    <ul class="li_2">
            <li class="li_1">Поиск Авиабилетов </li>
            <li class="li_1">HOME</li>
            <li class="li_1">CONTACTS   </li>
        </ul>
        </div>
        <div class="container">
        <div class="searchCity"> 
          <div class="departure">
          <h3>  Город вылета </h3>
        <VueSearchPanel />
        </div>
        <div class="arrive">
          <h3>Город прилета</h3>
        <VueSearchPanel />
        </div>
        </div>
        
     <div class="dateSelect">   
    <tickets />
    <tickets />
    </div>
    </div>
    </div>
  </div>
</template>

<script>
import tickets from './components/tickets.vue';
import VueSearchPanel from './components/menu.vue'






export default {
  data() {
    return {
      isActive: true
    }
  },
  name: 'App',
  components: {
    tickets,  VueSearchPanel 
  
    
    
  }
}
</script>

<style>


.hea{

	max-width: 800px;
	margin: 0 auto;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
	font-size: 20px;
	background:rgb(138, 0, 0);
  
  
}
.li_2{
	
	
	display: grid;
	grid-template-columns: 6fr 1fr 1fr;
}
.li_2 li{
	margin: 10px;
  
  
}
.li_1{
	
  list-style-type: none;
  color:white;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.li_1::first-letter{
  color:Black;
  font-family:cursive;
}
.li_1:hover{
  text-decoration: underline;
  color:black;
}
.dateSelect{
  max-width: 800px;
  margin:0 auto;
  display: flex;
  justify-content: space-around;
  background: rgb(138, 0, 0) ;
}
.searchCity{
  max-width: 800px;
  margin:0 auto;
  display: flex;
  justify-content: space-around;
  background: rgb(138, 0, 0);
  margin-top:0px;
  
}
.demo-comp{
  font-size:20px ;
}
.demo-comp button{
  padding: 5px;
  background:rgb(160, 224, 216);
  border-radius: 7px;
  border:solid;
  color:rgb(0, 0, 0);
}
.searchCity h3{
  margin-bottom: 5px;
  color:white;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.container{
  max-width: 800px;
  margin:0 auto;
  border:solid;
}
.mainn{
  max-width: 800px;
  margin:0 auto;
  background: rgb(138, 0, 0);
  
}
.v-calendar .input-field input{
  background: rgb(0, 0, 0);
 border:solid;
}
</style>
