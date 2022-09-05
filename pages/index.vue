<template>
  <main>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/">
                Inicio
              </NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/blog">
                Blog
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
<div class="container">
  <div class="row">
    <h1>Sitio</h1>
    <li v-for="article of articles" :key="article.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
          <div>
            <h2>{{ article.title }}</h2>
            <p>{{ article.description }}</p>
          </div>
        </NuxtLink>
      </li>
  </div>
  
</div>
  
 
  </main>
</template>

<script>
  export default {
    async asyncData({ $content, params }) {
      console.log($content)
      const articles = await $content('blog')
        .only(['title', 'slug'])
        .sortBy('createdAt', 'asc')
        .fetch()
      return {
        articles
      }
    }
  }
</script>