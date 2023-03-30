<template>
  <div>
    <button @click.prevent="handleClick">MS LOGIN</button>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      window.location.href=`https://login.microsoftonline.com/common/oauth2/v2.0/authorize
        ?client_id=${process.env.CLIENT_ID}
        &response_type=token
        &redirect_uri=http://localhost:3000/auth/token
        &scope=openid%20offline_access%20https%3A%2F%2Fgraph.microsoft.com%2Fmail.read
        &state=12345`
      // window.location.replace(`${process.env.MS_AUTH_URL}?client_id=${process.env.CLIENT_ID}&response_type=token&scope=user.read`)
    }
  }
}
</script>
