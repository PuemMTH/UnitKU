<template>
    <div class="grid grid-cols-3 gap-1 md:grid-cols-2">
        <div v-for="item in items" :key="item.id">
            <div class="m-2">
                <div class="flex justify-center">
                    <div class="flex flex-col md:flex-row md:max-w-xl rounded-lg bg-white shadow-lg ">
                        <img class="w-full h-96 md:h-auto object-cover md:w-48 rounded-t-lg md:rounded-none md:rounded-l-lg" :src="item.image" alt="" />
                        <div class="p-6 flex flex-col justify-start">
                            <h5 class="text-gray-900 text-xl font-medium mb-2 ">Card title</h5>
                            <p class="text-gray-700 text-base mb-4">
                                This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.
                            </p>
                            <p class="text-gray-600 text-xs">Last updated 3 mins ago</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'AnimeLoading',
    data() {
        return{
            items : [
                {image :"https://cdn.myanimelist.net/images/anime/1441/122795.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1143/121873.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1160/122627.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1995/121695.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1108/121157.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1612/120636.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1368/121281.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1120/120796.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1247/121345.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1934/122301.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1361/120706.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1285/120529.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1904/120095.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1970/122297.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1161/121462.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1347/120593.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1109/118948.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1423/122029.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1976/122302.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1093/121114.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1731/120871.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1054/121949.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1571/121381.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1036/121135.jpg"},
                {image :"https://cdn.myanimelist.net/images/anime/1311/120270.jpg"},
            ]
        }
    }
}
</script>