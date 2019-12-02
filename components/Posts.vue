<template>
  <section class="main-content">
    <div class="container">
      <h1 class="title has-text-centered">Recent Posts.</h1>
      <div class="columns is-multiline">
        <div class="column is-half" v-for="post in posts" :key="post.id">
          <div class="card">
            <header class="card-header">
              <p class="card-header-title">{{post.title}}</p>
            </header>
            <div class="card-content">
              <div class="content">
                {{post.body}}
                <br />
                <small>
                  by
                  <strong>{{post.userId}}</strong>
                  \\ {{post.id}}
                </small>
              </div>
            </div>
            <footer class="card-footer">
              <nuxt-link :to="`/post/${post.id}`" class="card-footer-item">Read More</nuxt-link>
            </footer>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import axios from "axios";

export default {
  name: "posts",
  created() {
    return axios
      .get(`https://jsonplaceholder.typicode.com/posts`)
      .then(res => {
        this.posts = res.data;
      })
      .catch(e => {
        error({ statusCode: 404, message: "Post not found" });
      });
  },
  data() {
    return { posts: [] };
  }
};
</script>
