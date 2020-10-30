<template>
  <div id="app">
    <!-- <input type="text" v-model="title" /> -->
    <!--<input type="text" :value="title" @input = "title = $event.target.value" />-->
    <!--<editor v-model="content"></editor>-->
    <date-picker v-model="date"></date-picker>
  </div>
</template>

<script>
//import Editor from "./components/Editor"
import DatePicker from "./components/DatePicker"
export default {
  name: 'App',
  components: {
    //Editor,
    DatePicker
  },

  data() {
    return {
      title: "",
      content: "",
      date: {
        day: null,
        month: null,
        year: null
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
