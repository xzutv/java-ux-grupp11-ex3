<template>
    <div class="profession">

        <div class="units">
            <img :src="img_src" :alt="alt" style="padding: 0;">
            <label>{{ label }}</label>

            <div class="count-units">
                <img src="/src/assets/icons/Minus.svg" alt="minus" @click="decrease" style="cursor: pointer; padding:0;">
                <p>{{ count }}</p>
                <img src="/src/assets/icons/Plus.svg" alt="plus" @click="increase" style="cursor: pointer;">
            </div>
        </div>

        <div class="availability">
            <label><input type="radio">50%</label>
            <label><input type="radio">100%</label>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Profession',
    props: {
        img_src: {
            type: String,
            required: true
        },
        alt: {
            type: String,
            default: 'Bild'
        },
        label: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            count: 0
        }
    },
    methods: {
        increase() {
            this.count++
        },
        decrease() {
            this.count--
        }
    }
}
</script>

<style scoped>
div {
    background-color: blueviolet;
}

.units {
    display: flex;
    flex-direction: row;
}

.count-units {
    display:flex;
    flex-direction: row;
    padding: 0;

}

</style>