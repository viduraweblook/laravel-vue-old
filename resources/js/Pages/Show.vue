<template>
    <div class="blog_container">
        <h1>{{blogs.title}}</h1>
        <p>{{blogs.author}}</p>
        <div>
            {{ blogs.content }}
        </div>
    </div>

</template>

<script setup>
import{defineProps} from 'vue';

defineProps({
    blogs: Object
});
</script>
