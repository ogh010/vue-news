<template>
    <div>
        <ul class="news-list">
            <li v-for="item in ListItems" v-bind:key="item.title" 
                class="post">
                <!-- 포인트 영역 -->
                <div class="points">
                    {{item.points || 0}}
                </div>
                <!-- 기타 정보 영역 -->
                <div>
                    <p>
                        <template v-if="item.domain">
                            <a :href="item.url" >
                                {{item.title}}
                            </a>
                        </template>
                        <template v-else>
                            <router-link v-bind:to="`item/${item.id}`">
                                {{item.title}}
                            </router-link>
                        </template>
                    </p>
                    <small class="link-text">
                        {{item.time_ago}} by 
                        <router-link 
                        v-if="item.user"
                        v-bind:to="`/user/${item.user}`" class="link-text">
                            {{item.user}}
                        </router-link>
                        <a :href="item.url" v-else>
                            {{item.domain}}
                        </a>
                    </small>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    created(){
        // this.$store.dispatch('FETCH_NEWS')
        const name = this.$route.name;
        if(name === 'news'){
            this.$store.dispatch('FETCH_NEWS')
        }
        else if(name === 'ask'){
            this.$store.dispatch('FETCH_ASK')
        }
        else if(name === 'jobs'){
            this.$store.dispatch('FETCH_JOBS')
        }
    },
    computed:{
        ListItems(){
            const name = this.$route.name;
            if(name==='news'){
                return this.$store.state.news;
            }
            else if(name==='ask'){
                return this.$store.state.ask;
            }
            else{
                return this.$store.state.jobs
            }
        }
    }
}
</script>
<style scoped>
.post{list-style-type: none; display: flex; align-items: center;
border-bottom: 1px solid #eee;}
.points{width: 80px; height: 60px; display: flex; align-items: center;
justify-content: center; color: rgb(161, 135, 98);}
.news-title{margin: 0;;}
.link-text{color: rgb(153, 130, 99);}
</style>