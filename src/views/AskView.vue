<template>
    <div>
        <ListItem></ListItem>
        <!-- <ul class="news-list">
            <li v-for="item in fetchedAsk" v-bind:key="item.title"
                class="post">
                <div class="points">
                    {{item.points}}
                </div>
                <div>
                    <p class="news-title">
                        <router-link v-bind:to="`item/${item.id}`">{{item.title}}</router-link>
                    </p>
                    <small class="link-text">{{item.time_ago}} by {{item.user}}</small>
                </div>
            </li>
        </ul> -->
    </div>
</template>

<script>
import ListItem from '../components/ListItem'

export default{
    components:{
        ListItem,
    }
}
// import {mapGetters} from 'vuex'

// export default {
//     computed:{
//         ...mapGetters([
//             'fetchedAsk'
//         ])
//     },
//     created() {
//         this.$store.dispatch('FETCH_ASK')
//     },
// }
</script>
