<template>
  <NuxtLink :to="'/posts/' + id">
    <div class="post">
      {{ id }}) {{ title }}
    </div>
  </NuxtLink>
</template>

<script>
export default {
  name: 'Post',
  props: {
    id: String,
    title: String
  }
}
</script>

<style>
  .post {
    border: ridge 1px gray;
    padding: 10px;
    margin-top: 5px;
  }
  a {
    text-decoration: none;
  }
</style>
