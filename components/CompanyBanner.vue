<script setup>
    const companyLogo = [
        'google.png',
        'nike.png',
        'samsung.png',
        'apple.png',
        'adidas.png'
    ]
    const images = import.meta.glob('../assets/img/*.png', { eager: true });

    const getSrc = (fileName) => {
    // Construct the path and return the URL
        return images[`../assets/img/${fileName}`]?.default || '';
    };
</script>

<template>
    <div class="flex items-center justify-between mt-2 border-2 p-4 px-10">
        <div v-for="(cl, index) in companyLogo" :key="index">
            <img :src="getSrc(cl)" alt="">
        </div>
    </div>
</template>