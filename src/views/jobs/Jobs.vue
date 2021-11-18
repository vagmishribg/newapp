<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="jobs">
    <router-link :to="{name: 'JobsDetails',params: {id: job.id}}">
        <h2> {{job.title}}</h2>
    </router-link>
    </div>
</template>

<script>
import About from '../About.vue'
export default{
  components: { About },
    data() {
        return {
            jobs: [
                {title: 'Primary Jobs', id:1,details:'lorem'},
                {title: 'Secondary Jobs', id:2,details:'lorem'},
                {title: 'Tertiary Jobs', id:3,details:'lorem'},
            ]
        }
    }
}
</script>

<style>
 .jobs h2{
     background: #f4f4f4;
     padding: 10px;
     border-radius: 30px;
     margin: 30p auto;
     max-width: 1000px;
     cursor: pointer;
     color: #444;
 }
 .jobs h2.hover{
     background: #ddd;
 }
 .job a{
     text-decoration: none;
 }

</style>
