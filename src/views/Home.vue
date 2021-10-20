<template>
  <div class="home">
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";

export default {
  name: "Home",
  setup() {
    // const p = ref(null);

    const name = ref("mario");
    const age = ref(30);

    const handleClick = () => {
      name.value = "Luigi";
      age.value = 35;
    };

    return { name, age, handleClick };
  },
};
</script>
