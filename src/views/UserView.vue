<template>
    <div>
        <UserProfile></UserProfile>
        <!-- <p>name : {{userInfo.id}}</p>
        <p>created : {{userInfo.created}}</p>
        <p>karma : {{userInfo.karma}}</p> -->
    </div>
</template>
<script>
import UserProfile from '../components/UserProfile.vue'

export default {
    computed:{
        userInfo(){
            return this.$store.state.user;
        }
    },
    created() {
        const userName = this.$route.params.id;
        this.$store.dispatch('FETCH_USER',userName)
    },
    components:{
        UserProfile
    }
}
</script>
<style scoped>

</style>