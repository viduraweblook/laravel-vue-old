<template>
    <div>
        <table class="table">
            <thead class="thead-dark">
              <tr>
                <th scope="col">ID</th>
                <th scope="col">Name</th>
                <th scope="col">Phone</th>
                <th scope="col">Details</th>
                <th scope="col">Read</th>
                <th scope="col">Edit</th>
                <th scope="col">Delete</th>
              </tr>
            </thead>

            <tbody class="blog_block" v-for="customers in customer" :key="customers.id">
              <tr>
                    <th scope="row">{{ customers.id }}</th>
                    <td> {{ customers.cname }} </td>
                    <td> {{ customers.cphonenum }} </td>
                    <td> {{ customers.cdetails }} </td>
                    <td> <Link :href="`/blog/`">Read More</Link> </td>
                    <td> <Link :href="`/blog/edit/`">Edit Post</Link></td>
                    <td> <Link :href="`/blog/delete/`" method="DELETE">Delete Post</Link> </td>
              </tr>
            </tbody>
          </table>
    </div>
</template>

<script>
import { Link } from '@inertiajs/vue3';
export default {
    components:{
        Link
    },
props:{
    customer:{
        type:Array,
        default:[]
    }
}
}
</script>

<style>
</style>
