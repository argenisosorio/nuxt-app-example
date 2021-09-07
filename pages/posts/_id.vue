<template>
  <div>
    <h1>Post detail</h1>
    <h2>{{ post.id }}) {{ post.title }}</h2>
    <p>{{ post.body }}</p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  layout: 'navbar',
  data () {
    return {
      post: {}
    }
  },
  async created () {
    const resp = await axios.get('https://jsonplaceholder.typicode.com/posts/' + this.$route.params.id)
    this.post = resp.data
  }
}
</script>
