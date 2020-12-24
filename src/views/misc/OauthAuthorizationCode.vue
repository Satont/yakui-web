<template>
  <div></div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class extends Vue {
  created () {
    const query = this.$route.query
    const code = query.code
    const state = query.state as string
    const encodedState = JSON.parse(window.atob(state))

    if (!code || !state || !encodedState.original) return

    window.location.replace(`${encodedState.original}/twitch/auth/callback?code=${code}&state=${state}`)
  }
}
</script>
