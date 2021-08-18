<template>
    <div>
      <h1>This is an About Page</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque est id repellat explicabo dolorum. Non consequatur quae delectus voluptates modi ipsam labore provident, inventore rerum et tempore, a incidunt exercitationem?</p>
    </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'About the app',
      meta: [{
        hid: 'description',
        name: 'description',
        content: 'My first nuxt application'
      }]
    }
  }
}
</script>

<style>

</style>
