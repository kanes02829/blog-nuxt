<template>
  <section class="main-content">
    <div class="container">
      <h1 class="title has-text-centered">Recent Posts.</h1>
      <div class="columns is-multiline">
        <div class="column is-half">
          <div class="card">
            <header class="card-header">
              <p class="card-header-title">Título</p>
            </header>
            <div class="card-content">
              <div class="content">
                Sumário
                <br />
                <small>
                  by
                  <strong>Autor</strong>
                  \\ Publicado
                </small>
              </div>
            </div>
            <footer class="card-footer">
              <a href="/post/id" class="card-footer-item">Read More</a>
            </footer>
          </div>
          <div class="card">
            <header class="card-header">
              <p class="card-header-title">Título</p>
            </header>
            <div class="card-content">
              <div class="content">
                Sumário
                <br />
                <small>
                  by
                  <strong>Autor</strong>
                  \\ Publicado
                </small>
              </div>
            </div>
            <footer class="card-footer">
              <a href="/post/id" class="card-footer-item">Read More</a>
            </footer>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "posts"
};
</script>
