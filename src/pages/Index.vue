<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

    <h1>Hello, world!</h1>

    <article>
      <section>
        <Posts v-for="edge in $page.allPost.edges" :key="edge.node.id" :post="edge.node"/>
      </section>
    </article>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
    </p>

    <p class="home-links">
      <a href="https://gridsome.org/docs/" target="_blank" rel="noopener">Gridsome Docs</a>
      <a href="https://github.com/gridsome/gridsome" target="_blank" rel="noopener">GitHub</a>
    </p>

  </Layout>
</template>

<script>
import Posts from "@/components/Posts";

export default {
  components: {
    Posts
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<page-query>
  query {
    allPost {
      totalCount
        edges {
          node {
            id
            title
            description
            date (format: "D MMMM YYYY")
            path
        }
      }
    }
  }
</page-query>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
