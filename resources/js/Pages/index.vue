<template>

<nav>
    <Link :href="`/blog/create`">Create</Link>
</nav>


<!-- <h1>hhh</h1> -->
    <div class="container mx-auto pt-5">
        <h1>Welcome</h1>
        <div class="blog_block" v-for="blog in blogs" :key="blog.id">
            <h2> {{ blog.title }} </h2>
            <p> {{ blog.author }} </p>
            <Link :href="`/blog/${blog.id}`">Read More</Link>
            <Link :href="`/blog/edit/${blog.id}`">Edit Post</Link>
            <Link :href="`/blog/delete/${blog.id}`" method="DELETE">Delete Post</Link>
        </div>
    </div>

</template>


<script setup>
import{defineProps} from 'vue';
import { Link } from '@inertiajs/vue3';
defineProps({
    blogs: Array
});
</script>
