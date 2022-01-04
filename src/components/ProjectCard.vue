<template>
    <div class='project-card' >
        
        <div class="project-body">
                <div class="project-header flex">
                <h2>{{project}}</h2>
                <i v-on:click="showOverlay = !showOverlay" class="fas fa-info-circle"></i>
            </div>
            
            <img  class="card-img"  :src="require(`../assets/${image}`)">
            
            <a href="">View Site</a>
            <a href="">View Repo</a>

            <div class="flex project-technologies"> 
                <div v-for="(item, index) in technologies" :key="index">
                    <span>{{item}}</span>
                </div>
            </div>
        </div>
        <div class='overlay' :class="showOverlay ? 'overlay-visible' : ''">
            <p>{{description}}</p>
            <button v-on:click="showOverlay = !showOverlay">&times;</button>
        </div>
        
        
    </div>
</template>

<script>
    export default {
        name: 'ProjectCard',
        props: {
            project: String,
            image: String,
            description: String,
            technologies: Array
        },
        data() {
            return{
                showOverlay: false
            }
        }
    }
</script>