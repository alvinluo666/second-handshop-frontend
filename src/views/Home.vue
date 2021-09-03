<template>
  <div class="home">
    <Banner></Banner>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Banner from '@/components/Home/Banner.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Banner
  }
}
</script>
