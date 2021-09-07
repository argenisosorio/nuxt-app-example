<template>
  <div>
    <h1>Blog</h1>
    <table class="table" border="1px">
      <thead>
        <tr>
          <th scope="col">
            ID
          </th>
          <th scope="col">
            TITLE
          </th>
          <th scope="col">
            BODY
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(post, index) in posts" :key="index">
          <td v-text="post.id" />
          <td v-text="post.title" />
          <td v-text="post.body" />
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from 'axios'
export default {
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
