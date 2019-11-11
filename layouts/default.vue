<template>
  <div>
    <Navbar />

    <main>
      <div class="container">
        <nuxt />
      </div>
    </main>
  </div>
</template>

<script>
import Navbar from '@/components/nav-bar'

export default {
  components: {
    Navbar
  }
}
</script>

