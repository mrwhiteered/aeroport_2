<template>
  <datepicker lang="ru"> </datepicker>
</template>


<script>
  import 'vue-datepicker-ui/lib/vuedatepickerui.css';
  import VueDatepickerUi from 'vue-datepicker-ui';

  export default {
    components: {
      Datepicker: VueDatepickerUi
    }
  }
</script>


<style >
.v-calendar {
    margin: 20px;
    border: solid black ;
    border-radius: 10px;
}

</style>