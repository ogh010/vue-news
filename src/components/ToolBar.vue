<template>
    <div class="header">
        <router-link to="/news">News</router-link> |
        <router-link to="/ask">Ask</router-link> |
        <router-link to="/jobs">jobs</router-link> 
    </div>
</template>
<script>
export default {
    
}
</script>
<style scope>
    .header{color: #fff; background-color: tan; display: flex; text-decoration: none; padding: 8px;;}
    .header a{color: #fff; margin: 0 10px;}
    .header .router-link-exact-active{color: rgb(112, 71, 17);}
    
</style> 