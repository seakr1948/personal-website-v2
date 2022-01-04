<template>
    <nav class='navbar' >
        <p>This is the {{msg}}</p>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    props: {
        msg: String
    }
}
</script>