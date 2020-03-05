<template type="text/x-template" id="card-template">
  <div>
    <h3>{{title}}</h3>
    <ul>
      <li v-for="(link,idx) in links" :key="idx">
        <a :href="link.url">{{link.text}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "CardItem",
  template: "#card-template",
  props: ["title", "links"]
};
</script>

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
