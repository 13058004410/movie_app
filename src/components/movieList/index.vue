<template>
    <div class="list">
        <ul>
            <li v-for='item in result' :key='item.id'>
                <div>
                    <img :src="item.poster|setWH(128*180)" alt="">
                </div>
                <div>
                    <h1></h1>
                    <p></p>
                </div>
                <div>
                    <button>观看</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name:'movieList',
        data(){
            return {
                result:[]
            }
        },
        mounted(){
            this.axios.get('http://v.juhe.cn/movie/index?title=%E8%80%85&smode=0&pagesize=&offset=&dtype=&key=ab2a5e3fd3b625c9a7ac728b5c325f4f').then((res)=>{
                var msg=res.data.result;
                if(msg==='ok'){
                    this.result=res.data.data.result;
                }
                
            })
            
        }
    }
</script>

<style>

</style>