<template>
    <div class="image-card">
        <div>
            <img :src="src" :alt="alt || 'Bild'" />
            {{ name }}
        </div>

    </div>
</template>

<script>


export default {
    name: 'custom-img',
    props: {
        src: {
            type: String,
            required: true
        },
        alt: {
            type: String,
            default: 'Bild'
        }
    },
}
</script>

<style scoped>
img {
    max-width: 100%;
    border-radius: 8px;
}
</style>