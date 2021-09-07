<template>
  <div>
    <h1>Blog</h1>
    <ul>
      <li>
        <NuxtLink to="/blog/post1">
          Post 1
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/blog/post2">
          Post 2
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/blog/post3">
          Post 3
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  layout: 'navbar'
}
</script>
