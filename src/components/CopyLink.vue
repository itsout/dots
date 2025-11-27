<template>
  <!-- Share link UI removed -->
</template>

<script>
export default {
  name: 'CopyLink',

  data () {
    return {
      gameLink: this.$GAME_INVITE_LINK + localStorage.getItem('gameCode')
    }
  },

  methods: {
    copyGameLink () {
      this.$buefy.toast.open({
        duration: 2000,
        message: 'Invite Link Copied !',
        position: 'is-top',
        type: 'is-success'
      })
    }
  }
}
</script>

<style scoped>
#linkInput {
  width: 70%;
}
</style>
