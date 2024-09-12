
<template>
    <div class="flex justify-between py-4">
        <div>
            <h1 @click="$router.push('/')">Logo</h1>
        </div>
        <ul class="flex space-x-4">
            <li><NuxtLink to="/about" >About</NuxtLink></li>
            <li><NuxtLink to="/work" >Work</NuxtLink></li>
            <li><NuxtLink to="/contact" >Contact</NuxtLink></li>
        </ul>
    </div>
</template>