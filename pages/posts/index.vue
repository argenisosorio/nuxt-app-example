<template>
  <div>
    <h1>Posts</h1>
    <Post
      v-for="(post, index) in posts"
      :id="post.id"
      :key="index"
      :title="post.title"
    />
  </div>
</template>

<script>
import axios from 'axios'
import Post from '../../components/Post'
export default {
  components: {
    Post
  },
  layout: 'navbar',
  data () {
    return {
      posts: []
    }
  },
  async created () {
    const resp = await axios.get('https://jsonplaceholder.typicode.com/posts')
    this.posts = resp.data
  }
}
</script>
