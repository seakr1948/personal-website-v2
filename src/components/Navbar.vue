<template>
    <nav class='navbar flex' >
        <div class="initials flex">
            <button
                        @click="() => {clickOpen = !clickOpen }" 
                                class="fas fa-bars">
            </button>
            <p>FN</p>
        </div>
        <div class="links">
           <ul class="flex">
               <li><a href="#welcome-section">Welcome</a></li>
               <li><a href="#about-me">About Me</a></li>
               <li><a href="#projects">Projects</a></li>
               <li><a href="#skills">Skills</a></li>
               <li><a href="#contact">Contact</a></li>
           </ul>
        </div>
    </nav>
</template>

<script> 


export default {
    name: 'Navbar',
    props: {
        sidenav_open: Boolean
    },
    data() {
        return{
            clickOpen: false
        }
    },
    mounted() {
        this.clickOpen = this.sidenav_open
    },
    watch: {
        clickOpen: function(new_val, old_val){
            console.log(new_val, old_val);
            this.$emit('toggleState', new_val);
        },
        sidenav_open: function(){
            this.clickOpen = this.sidenav_open
        }
    }

}
</script>