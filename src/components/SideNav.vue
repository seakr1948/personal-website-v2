<template>

    
    <div :class="`side-nav ${sidenav_open ? 'side-nav-open' : ''}`">
        <button class="far fa-times-circle"  @click="() => {clickClosed = !clickClosed }" ></button>
        <ul class="">
               <li><a href="#welcome-section">Welcome</a></li>
               <li><a href="#about-me">About Me</a></li>
               <li><a href="#projects">Projects</a></li>
               <li><a href="#skills">Skills</a></li>
               <li><a href="#contact">Contact</a></li>
           </ul>
    </div>
</template>

<script>
    export default {
        props: {
        sidenav_open: Boolean
    },
    data() {
        return{
            clickClosed: false
        }
    },
    mounted() {
        this.clickClosed = this.sidenav_open
    },
    watch: {
        clickClosed: function(new_val, old_val){
            console.log(new_val, old_val);
            this.$emit('toggleState', new_val);
        },
        sidenav_open: function(){
            this.clickClosed = this.sidenav_open;
        }
    }
    }
</script>