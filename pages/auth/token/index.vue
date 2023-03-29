<template>
  <div>
    TOKEN
  </div>
</template>

<script>
import jwt_decode from "jwt-decode";

export default {
  created() {
    const first = this.$route.hash.split('&')[0].split('=')[1]

  }
}
</script>
