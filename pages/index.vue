<template>
  <div>
    <button @click.prevent="handleClick">MS LOGIN</button>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      // window.location.replace(`${process.env.MS_AUTH_URL}?client_id=${process.env.CLIENT_ID}&response_type=token&scope=user.read`)
      console.log(this.$route.fullPath)
    }
  }
}
</script>
