<template>
  <Layout>
    <h1>Liste des projets </h1>
    <ul>
      <li v-for="{node:projet} of $page.allProjet.edges" :key="projet.Id">
        <g-link :to="projet.path">{{ projet.title }}</g-link>
      </li>
    </ul>
  </Layout>
</template>

<page-query>
query {
  allProjet {
    edges {
      node {
      id
      path
      title
      }
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>
