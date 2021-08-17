<template>
  <h1>This is an a Single User, with id: {{ $route.params.id }}</h1>
</template>

<script>
export default {
  validate(data) {
    return /^\d+$/.test(data.params.id)
  },

  layouts: 'users'
}
</script>

<style>

</style>