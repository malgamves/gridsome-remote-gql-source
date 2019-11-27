<template>
  <Layout>
    <h1>About us</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
    <h1>Books Read by Me</h1>
    <div v-for="book in $page.books" v-bind:key="book.id">
      <li>{{ book.author}} - {{ book.name}}</li>
    </div>
  </Layout>
</template>


<page-query>  
query {
  books {
    author
    id
    name
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: "About us"
  }
};
</script>
