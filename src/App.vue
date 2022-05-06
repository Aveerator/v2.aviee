<script lang="js">
import SpinnerOne from "./components/SpinnerOne.vue";


function addElement(yes){
    var yees = document.getElementById("text").value;
    yes.push(yees);
    console.log(yes);
}

export default {
  name: "App",
  methods: {
    addElement: addElement
  },
  components: {
    SpinnerOne,
  },
  data() {
    return {
      items: ["Add new spinny bois into the << input and apply!"],
    };
  },
};
</script>

<template>
  <input type="text" id="text" />
  <button @click="addElement(items)" class="addbutton">Apply</button>
  <div class="body">
    <SpinnerOne v-for="(text, index) in items" :key="index">{{
      text
    }}</SpinnerOne>
  </div>
</template>

<style lang="scss">
.addbutton {
  background-color: transparent;
  color: black;
  border: 0mm;
}
.addbutton:hover {
  background-color: black;
  color: white;
}
</style>
