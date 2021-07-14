<template>
  <p :class="['todo-item', todoProps.completed ? 'is-completed' : '']" :id="new_id">
      <input type="checkbox" :checked="todoProps.completed">
      {{ todoProps.title }}
      <button class="del-btn">Delete</button>
  </p>
</template>

<script>
import {ref} from 'vue';

export default {
    name: 'TodoItem',
    props: ['todoProps'],
    setup() {
        const new_id = ref('my-new-id');
        return {
            new_id
        }
    }
}
</script>

<style>
.todo-item {
    background: #f4f4f4;
    padding: 20px;
    margin: 0;
    border-bottom: 1px #ccc solid;
}

.is-completed {
    text-decoration: line-through;
}

.del-btn {
    background: #ff0000;
    color: #fff;
    border: none;
    cursor: pointer;
    float: right;
}
</style>