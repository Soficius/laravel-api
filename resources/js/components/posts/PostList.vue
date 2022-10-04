<template>
    <div>
        <h2 class="text-center">Posts</h2>
        <div v-if="posts.length">
            <PostCard  v-for="post in posts" :key="post.id" :post="post"/>
        </div>
        <h3 v-else>Nessun Post</h3>
    </div>
</template>

<script>
import PostCard from './PostCard.vue';
export default {
    name: "PostList",
    data() {
        return { posts: [] };
    },
    methods: {
        fetchPosts() {
            axios.get("http://localhost:8000/api/posts").then((res) => {
                this.posts = res.data;
            })
                .catch((err) => {
            })
                .then(() => {
            });
        },
    },
    mounted() {
        this.fetchPosts();
    },
    components: {
        PostCard
    }
};
</script>
