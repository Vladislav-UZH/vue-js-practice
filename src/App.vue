<template>
  <nav>
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
  </nav>
  <CommentForm @create="createComment" />
  <CommentsList :comments="comments" @delete="deleteComment"/>
  <!-- <router-view/> -->
</template>
<script>
import CommentsList from "@/components/CommentsList";
import CommentForm from "@/components/CommentForm";



export default {
  components: {
    CommentsList, CommentForm
},data() {
   return  {comments: [{
"postId": 1,
"id": 1,
"name": "id labore ex et quam laborum",
"email": "Eliseo@gardner.biz",
"body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
},
{
"postId": 1,
"id": 2,
"name": "quo vero reiciendis velit similique earum",
"email": "Jayne_Kuhic@sydney.com",
"body": "est natus enim nihil est dolore omnis voluptatem numquam\net omnis occaecati quod ullam at\nvoluptatem error expedita pariatur\nnihil sint nostrum voluptatem reiciendis et"
},
{
"postId": 1,
"id": 3,
"name": "odio adipisci rerum aut animi",
"email": "Nikita@garfield.biz",
"body": "quia molestiae reprehenderit quasi aspernatur\naut expedita occaecati aliquam eveniet laudantium\nomnis quibusdam delectus saepe quia accusamus maiores nam est\ncum et ducimus et vero voluptates excepturi deleniti ratione"
},
{
"postId": 1,
"id": 4,
"name": "alias odio sit",
"email": "Lew@alysha.tv",
"body": "non et atque\noccaecati deserunt quas accusantium unde odit nobis qui voluptatem\nquia voluptas consequuntur itaque dolor\net qui rerum deleniti ut occaecati"
},
{
"postId": 1,
"id": 5,
"name": "vero eaque aliquid doloribus et culpa",
"email": "Hayden@althea.biz",
"body": "harum non quasi et ratione\ntempore iure ex voluptates in ratione\nharum architecto fugit inventore cupiditate\nvoluptates magni quo et"
},]}
  },
  methods: {
    createComment(comment){
      this.comments.push(comment)
    },
    deleteComment(id){
      console.log(id);
      this.comments.filter(comment=>comment.id !== id)
    }
  }
}

</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
