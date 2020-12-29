<template>
  <tr>
    <td>
      <p v-html="post.date" />
    </td>

    <td>
      <g-link :to="post.path">
        <p v-html="post.title" />
      </g-link>
    </td>
  </tr>
</template>

<script>
export default {
  props: ["post"],
}
</script>
