<template>
    <form @submit.prevent="form.post('/blog')">
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
        <button type="submit" :disabled="form.processing">Create</button>
      </form>
</template>

<script setup>
import { useForm } from '@inertiajs/vue3'

const form = useForm({
  title: '',
  author: '',
  content: '',
})
</script>
