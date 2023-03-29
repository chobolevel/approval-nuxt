<template>
  <div>
    TOKEN
  </div>
</template>

<script>

export default {
  async asyncData({query, $axios}) {
    const { code } = query
    const data = await $axios.post('/login/token', {

    })
    console.log(data)
  },
}
</script>
