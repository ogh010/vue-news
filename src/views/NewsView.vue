<template>
    <div>
        <ListItem></ListItem>
        <!-- <ul class="news-list">
            <li v-for="item in this.$store.state.news" v-bind:key="item.title" 
                class="post">
                <div class="points">
                    {{item.points}}
                </div>
                <div>
                    <p class="news-title">
                        <a :href="item.url">
                            {{item.title}}
                        </a>
                    </p>
                    <small class="link-text">
                        by <router-link v-bind:to="`/user/${item.user}`" class="link-text">{{item.user}}</router-link>
                    </small>
                </div>
            </li>
        </ul> -->
    </div>
</template>

<script>
import ListItem from '../components/ListItem.vue'

export default{
    components:{
        ListItem
    }
}

</script>
