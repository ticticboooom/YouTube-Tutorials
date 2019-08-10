<template>
  <div id="app">
    <input type="text" v-model="title"/>
    <button @click="list.push(title)">Add</button>
    <div v-for="(item, index) in list" :key="index">
      <TodoListItem :title="item"></TodoListItem>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoListItem from "./components/TodoListItem.vue";
@Component({
  components:{
    TodoListItem
  }
})
export default class App extends Vue {
  private item: string = ""; 
  private list: string[] = [];
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
