<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Text Input</h2>

    <input v-model="text"> {{ text }}

    <h2>Checkboxes</h2>
    <input type="checkbox" id="checkbox1" v-model="check">
    <label for="checkbox">Check: {{check}}</label>

    <ul>
      <li v-for="x in lists">
        {{ x.name }}
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      text: 'Test1',
      check: false,
      lists: [
        { name: 'John Doe'},
        { name: 'Jane Doe'},
        { name: 'Jan Doe'},
        { name: 'Jash Doe'},
      ]
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
