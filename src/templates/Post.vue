<template>
  <Layout>
    <g-link to="/" class="link">  &larr; Go Back</g-link>

    <h1>{{$page.post.title}}</h1>

    <p>Posted: {{ $page.post.date}}.</p>

    <p v-html="$page.post.content" />
  </Layout>
</template>

<page-query>
  query Post ($path: String!) {
    post: post (path: $path) {
      id
      title
      content
      date (format: "D MMMM YYYY")
    }
  }
</page-query>
