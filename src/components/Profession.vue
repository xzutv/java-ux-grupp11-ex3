<template>

    <div :class="['profession', { active: count > 0 }]">

        <div class="units">
            <img :src="img_src" :alt="alt" class="icon" :class="{ 'icon-dark': count > 0, 'icon-light': count === 0 }">
            <label>{{ label }}</label>

            <div class="count-units">

                <button class="circle-button" :class="{ disabled: count === 0 }" @click="decrease"
                    :disabled="count === 0">
                    <img src="/src/assets/icons/Minus.svg" alt="minus" class="plus-minus-icon">
                </button>

                <p>{{ count }}</p>

                <button class="circle-button" @click="increase">
                    <img src="/src/assets/icons/Plus.svg" alt="plus" class="plus-minus-icon">
                </button>

            </div>
        </div>

        <div class="availability">
            <label><input type="radio" name="availability" value="50">50%</label>
            <label><input type="radio" name="availability" value="100">100%</label>
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
            if (this.count > 0) {
                this.count--
            }
        }
    }
}
</script>

<style scoped>
.profession {
    background-color: #ffffff;
    padding: 12px;
    border-radius: 12px;
    color: #000;
    transition: background-color 0.3s ease;
    display: inline-block;
}

.profession.active {
    background-color: #242038;
    color: white;
}

.units {
    display: flex;
    align-items: center;
    gap: 15px;
}

.icon {
    width: 20px;
    height: 20px;
}

.icon-light {
    filter: brightness(0) saturate(100%) invert(0%);
}

.icon-dark {
    filter: brightness(0) saturate(100%) invert(100%);
}

.count-units {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 8px;
}

.circle-button {
    background-color: #f0f0f0;
    border: none;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}


.circle-button img {
    width: 10px;
    height: 10px;
}

.circle-button.disabled {
    opacity: 0.4;
    cursor: not-allowed;
}

.availability {
    margin-top: 8px;
    display: flex;
    gap: 12px;
}

input[type="radio"] {
    margin-right: 4px;
}
</style>