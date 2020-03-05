<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <CardItem title="My Card Item" :links="links"/>
    <CardItem title="My Card Item" links="[{text:'abc', url:'abc'}]"/>
  </div>
</template>

<script>
import CardItem from "./Card.vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: function() {
    return {
      links: [
        { text: "test", url: "http://test" },
        { text: "google", url: "http://google.com.au" }
      ]
    };
  },
  components: {
    CardItem
  }
};
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
