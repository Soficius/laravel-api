<template>
    <div class="content">
        <AppHeader :title="title" />
        <main class="container mt-4">
            <PostList/>
        </main>
    </div>
</template>

<script>
import AppHeader from './AppHeader.vue';
import PostList from './posts/PostList.vue';
export default {
    name: "App",
    data() {
        return {
            title: "Boolpress"
        };
    },
    components: {
    AppHeader,
    PostList,
}
};
</script>
