<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
function deleteItem(index) {
    items.value.splice(index, 1);
}

function add() {
    items/value.push(newItem.value);
    newItem.value = '';
}
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item, index) in items" :key="index">
            {{ item }}
            <button @click="deleteItem(index)">Delete</button>
        </li>
     </ul>
     <input v-model="newItem" @keydown.enter="add" placeholder="Add new item" />
        <button @click="add">Add!</button>
   
</template>
