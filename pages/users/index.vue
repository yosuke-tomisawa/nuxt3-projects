<template>
  <div>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.id }}, {{ user.name }}
      </li>
    </ul>
    <img
      src="~/assets/janko-ferlic-ZzVMNgg23pk-unsplash.jpg"
      alt="cycle on girl"
    />
  </div>
</template>
<script setup>
const { data: users } = await useFetch(
  "https://jsonplaceholder.typicode.com/users"
);
</script>
