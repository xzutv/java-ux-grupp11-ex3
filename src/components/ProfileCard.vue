<template>
    <div class="image-card">
        <img :src="src" :alt="alt" />
        <label>{{ name }}</label>
    </div>
    <div class="profession-icon">
        <img src=""> <!-- idk yet -->
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
        },
        name: {
            type: String,
            required: true
        }
    },
}
</script>

<style scoped>
img {
    max-width: 60%;
    border-radius: 8px;
    /* margin-left: 10px; */
}

.image-card {
    display:flex;
    flex-direction: column;
    justify-items: center;
}

.label {
    width: 5rem;
}

</style>