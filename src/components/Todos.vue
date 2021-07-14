<template>
  <p v-for="todo in todos" v-bind:key="todo">{{todo}}</p>
</template>

<script>
import {ref} from 'vue'

export default {
    name: 'Todos',
    setup() {
        const todos = ref(['Việc 1', 'Việc 2', 'Việc 3'])
        return {
            todos,
        }
    }
}
</script>

<style>

</style>