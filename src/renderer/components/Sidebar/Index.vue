<template>
  <article class="tile is-child box">
    <button class="button is-dark" @click="promptNewBlock">
      New Block
    </button>
    <hr>
    <aside class="menu">
      <ul class="menu-list">
        <li><a>List One</a></li>
        <li><a>List Two</a></li>
      </ul>
    </aside>
  </article>
</template>

<script>
export default {
  methods: {
    promptNewBlock () {
      this.$dialog.prompt({
        message: `What's your name?`,
        inputAttrs: {
          placeholder: 'e.g. Walter',
          maxlength: 10
        },
        onConfirm: (value) => this.$toast.open(`Your name is: ${value}`)
      })
    }
  }
}
</script>

<style>

</style>
