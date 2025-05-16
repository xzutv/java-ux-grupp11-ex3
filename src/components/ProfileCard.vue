<template>
    <div class="profile">
        <div class="image-card">
            <img :src="src" :alt="alt" />
            <label>{{ name }}</label>
        </div>
        <div class="profession-icon">
            <img :src="icons"> <!-- idk yet --> 
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
        },
        name: {
            type: String,
            required: true
        },
        icons: [],

    },
}
</script>

<style scoped>
img {
    max-width: 1.5rem;
    border-radius: 8px;
    margin-left: 10px;
    /* width: 33px;
    height: 33px;
    flex-shrink: 0; */
}

.image-card {
    width: 5rem;
    height: 2rem;
    display: flex;
    flex-direction: column;
    justify-items: center;
}

/* .label {
    width: 7rem;
} */
</style>