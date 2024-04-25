<template>
    <form @submit.prevent="form.put(`/blog/update/${blog.id}`)">
        <div>
            <label for="">Title</label>
            <input type="text" v-model="form.title">
        </div>


        <div>
            <label for="">Author</label>
            <input type="text" v-model="form.author">
        </div>


        <div>
            <label for="">Content</label>
            <textarea name="" id="" cols="100" rows="5" v-model="form.content"></textarea>
        </div>

        <!-- submit -->
        <button type="submit" :disabled="form.processing">Edit</button>
      </form>
</template>

<script setup>
import { useForm } from '@inertiajs/vue3'
import { defineProps } from 'vue';

let props = defineProps({
    blog: Object
})

const form = useForm({
  title: props.blog ? props.blog.title : '',
  author: props.blog ? props.blog.author : '',
  content: props.blog ? props.blog.content : '',
});

</script>
