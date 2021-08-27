<template>
  <div>
    <button class="button" @click="count++">
      You clicked me {{ count }} times.
    </button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      count: 0
    }
  }
}
</script>
