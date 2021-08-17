<template>
    <div class="home-page">
      <section class="intro">
        <h1>Get the Latest Tech News!</h1>
      </section>
      <section class="featured-post">
        <PostPreview 
        id="1"
        thumbnail="https://images.unsplash.com/photo-1530893609608-32a9af3aa95c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
        title="Hello There"
        previewText="This is my first blog"/>
        <PostPreview 
        id="2"
        thumbnail="https://images.unsplash.com/photo-1530893609608-32a9af3aa95c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
        title="Hello There, the second time"
        previewText="This is second first blog"/>
        <PostPreview 
        id="3"
        thumbnail="https://images.unsplash.com/photo-1530893609608-32a9af3aa95c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
        title="Hii.."
        previewText="This is third first blog"/>
      </section>
    </div>
</template>

<script>
import PostPreview from '../components/Posts/PostPreview.vue'
export default {
  components: {
    PostPreview
  }
}
</script>

<style scoped>
    .intro {
      height: 300px;
      position: relative;
      padding: 30px;
      box-sizing: border-box;
      background-position: center;
      background-size: cover;
    }

    .intro h1 {
      position: absolute;
      top: 10%;
      left: 5%;
      width: 90%;
      font-size: 1.5rem;
      color: black;
      background-color: rgb(211, 211, 211);
      padding: 10px;
      border-radius: 10px;
      box-shadow: 3px 3px 3px black;
      box-sizing: border-box;
      border: 1px solid black;
    }

    @media (min-width: 768px) {
      .intro h1 {
        font-size: 2rem;
      }
    }

    .featured-posts {
      display: flex;
      padding: 20px;
      box-sizing: border-box;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
    }
</style>
