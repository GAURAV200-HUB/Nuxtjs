<template>
    <div>
      <h1>Welcome to Nuxt Application</h1>
    </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Welcome to Nuxt',
      meta: [{
        hid: 'description',
        name: 'description',
        content: 'My first nuxt application'
      }]
    }
  }
}
</script>
