<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const newItem = ref('')

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <template v-for="(item, index) in items" :key="item">
        <li>{{ item }}
        <button @click="items.splice(index, 1)">
            Delete!
        </button>
        </li>
        </template>
    </ul>
    <input type="text" v-model="newItem"><button @click="items.push(newItem)">Add!</button>

   
</template>
