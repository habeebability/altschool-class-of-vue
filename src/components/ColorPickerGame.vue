<script setup>
import { ref, reactive } from "@vue/reactivity";
import useColorPickerGame from "../composables/ColorPickerGame";

const { colors, message, matchColor } = useColorPickerGame();

// export default {
//   setup() {
//     const colors = ["green", "red", "blue", "purple"];
//     let message = ref("Pick a color...");

//     const matchColor = (value) => {
//       // do a random color based on the array index;
//       const randomNumber = Math.floor(Math.random() * 3) + 1; //between 1 - 4

//       if (colors[randomNumber] === value) {
//         message.value = `You win... [answer: ${colors[randomNumber]}]`;
//         return;
//       }

//       message.value = `You loose [answer: ${colors[randomNumber]}]`;
//     };

//     return { colors, message, matchColor };
//   },
// };
</script>

<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">{{ color }}</button>
</template>



<style></style>
