<template>
  <div>
    TOKEN
  </div>
</template>

<script>
export default {
  async created() {
    const token = this.$route.hash.split('&')[0].split('=')[1]
    await this.$cookies.set("_ac_tk", token)
    const { data } = await this.$axios.get('/graph/me', {
      headers: {
        Authorization: `Bearer ${token}`
      }
    })
    console.log(data.mail)
    console.log(data.mobilePhone)
    console.log(data.displayName)
    console.log(data.id)
  }
}
</script>
