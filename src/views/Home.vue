<template>
  <div class="home">
    <Landing/>
    <Content/>
  </div>
</template>

<script>
// @ is an alias to /src
import Landing from '@/components/Landing.vue'
import Content from '@/components/Content.vue'

export default {
  name: 'Home',
  components: {
    Landing, Content
  }
}
</script>
