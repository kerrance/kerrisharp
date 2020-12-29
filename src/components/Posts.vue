<template>
  <section>
    <p v-html="post.date" />
    <h1 v-html="post.title" />
    <p v-html="post.description" />
    <g-link :to="post.path">Read More...</g-link>
  </section>
</template>

<script>
export default {
  props: ["post"],
}
</script>
