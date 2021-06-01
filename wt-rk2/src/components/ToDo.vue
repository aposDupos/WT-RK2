<template>
  <div class="todo">
    <form class="form">
      <label for="input">Введите значение</label>
      <input type="text" id="input" v-model="item">
      <button @click="add" type="button">Добавить</button>
    </form>
    <ol class="todo-ol" v-if="itemList.length">
      <li class="todo-li" v-for="(elem, key) in itemList" :key="key">{{elem}}</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "ToDo",
  data() {
    return {
      item: '',
      itemList:[]
    }
  },
  methods: {
    add(){
this.itemList.push(this.item)
      this.item=''
    }
  }
}
</script>

<style lang="scss" scoped>
input{
  padding: 1em;
  font-size: 16px;
}
button{
  margin-top: 1em;
  height: 40px;
  width: 160px;
  background: #3D405B;
  color: #F2CC8F;
  outline: none;
  border: 0;
  border-radius: 5px;
  cursor: pointer;
}
.todo{
  margin-bottom: 1em;
}
</style>