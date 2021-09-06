<template>
  <section>
    <h1>{{ title }}</h1>
    <p>{{ content }}</p>
  </section>
</template>

<script>
export default {
  props: {
    title: { type: String, required: true },
    content: { type: String, required: false }
  }
}
</script>
