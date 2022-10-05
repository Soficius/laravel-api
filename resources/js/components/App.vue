<template>
    <div class="content">
        <AppHeader :title="title" />
        <main class="container mt-4">
            <HomePage/>
        </main>
    </div>
</template>

<script>
import AppHeader from './AppHeader.vue';
import HomePage from './pages/HomePage.vue';
export default {
    name: "App",
    data() {
        return {
            title: "Boolpress"
        };
    },
    components: {
    AppHeader,
    HomePage
}
};
</script>
