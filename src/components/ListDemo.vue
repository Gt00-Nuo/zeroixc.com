<script>
export default {
    data() {
        return {
            names:["test1","test2","test3"],
            result:[
                {
                    "id":3671371,
                    "urlSrc":"https://bbs.qyer.com/thread-3671371-1.html",
                    "title":"告诉你一个真实的伊拉克——伊拉克全景半自驾游，绝对开荒贴（完）",
                    "avator":"https://pic.qyer.com/album/user/4104/40/RUhVRh4HZEA/index?imageMogr2/thumbnail/2400x1204/crop/!2368x788a0a272/format/webp"
                },
                {
                    "id":3668522,
                    "urlSrc":"https://bbs.qyer.com/thread-3668522-1.html",
                    "title":"落日.帆船-2023年3月菲律宾8日游(含攻略总结)（完结）",
                    "avator":"https://pic.qyer.com/album/user/4097/35/RUlcRRkCZEA/index?imageMogr2/thumbnail/2400x1492/crop/!2396x796a4a364/format/webp"
                },
                {
                    
                    "id":3642622,
                    "urlSrc":"https://bbs.qyer.com/thread-3642622-1.html",
                    "title":"夏天去新疆看雪山花海--2022年夏游独库公路/唐布拉/巴音布鲁克/那拉提/喀拉峻/琼库什台/夏塔/伊昭公路/果赛景区",
                    "avator":"https://pic.qyer.com/album/user/4095/15/RUlcRxsCaEw/index?imageMogr2/thumbnail/2396x1348/crop/!2396x796a0a260/format/webp"
                }
            ],
            userInfo:{
                name:"iwen",
                age:20,
                sex:"沃尔玛购物袋"
            },            
        }
    }
}
</script>

<template>
    <h3>列表渲染</h3>
    <p v-for="(item , index) in names" :key="item">{{ index + 1 }}.{{ item }}</p>
    <!-- 也可以用 of 作为分隔符来替代 in  -->
    <!-- <p v-for="(item , index) of names" :key="item">{{ index + 1 }}.{{ item }}</p> -->
    <div v-for="item in result" :key="item">
        <p>{{ item.title }}//原帖：{{ item.urlSrc }}</p>
        <img :src="item.avator" alt="" width="100%">
    </div>
    <div v-for="(value,key,index) in userInfo" :key="index">{{ index }}.{{ key }}:&nbsp;{{ value }}</div>
</template>