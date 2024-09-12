<script setup>
const works = [
    'img0.png',
    'img1.png',
    'img2.png',
    'img3.png',
    'img4.png',
    'img5.png'
]

const images = import.meta.glob('../assets/img/*.png', { eager: true });

const getSrc = (fileName) => {
// Construct the path and return the URL
    return images[`../assets/img/${fileName}`]?.default || '';
};

</script>
<template>
    <div class="grid grid-cols-3 gap-4 border-2 px-10 text-xs">
        <div class="col-span-3 text-center font-semibold text-xl"><h1>Latest Works</h1></div>
        <div v-for="img in works" class="space-y-2">
            <div><img :src="getSrc(img)" alt=""></div>
            <div>
                <h1 class="font-semibold">Project title</h1>
                <p>Ui, Art drection</p>
            </div>
        </div>
    </div>
</template>