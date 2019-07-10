<template>
  <div class="hello">
    <h1>{{myvalue}}---{{msg }}</h1>
    <slot name="header"> noheader</slot>
    <input v-model="msg" />
    <slot name="footer"> nofooter</slot>
    <ul>
      <p v-for="item in data" @click="onClick">{{item.name}}-{{item.age}}</p>
    </ul>
  </div>
</template>

<script>
export default {
  props:['data','myvalue'],
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    onClick(){
      this.$emit('commonEvent',this.msg)
    }
  },
  created(){
    console.log(this.myvalue)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
