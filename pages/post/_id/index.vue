<template>
  <div class="main-content">
    <div class="container">
      <h2 class="title is-2">{{post.title}}</h2>
      <div v-html="post.body"></div>
      <br />
      <h4 class="title is-5 is-marginless">
        by
        <strong>Author {{post.userId}}</strong> at
        <strong>Published {{post.id}}</strong>
      </h4>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  head() {
    return {
      title: this.post.name,
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.post.year
        }
      ]
    };
  },
  validate({ params }) {
    return /^\d+$/.test(params.id);
  },
  asyncData({ params, error }) {
    return axios
      .get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
      .then(res => {
        return { post: res.data };
      })
      .catch(e => {
        error({ statusCode: 404, message: "Post not found" });
      });
  }
};
</script>