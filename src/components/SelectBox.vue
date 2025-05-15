<template>
    <div class="select-box">
        <div class="box">

            <select :value="modelValue" @change="$emit('update:modelValue', $event.target.value)">
                <option disabled value=""> {{ label }} </option>
                <option v-for="option in options" :key="option.id" :value="option.id">
                    {{ option.name }}
                </option>
            </select>
        </div>

    </div>
</template>

<script>

export default {
    name: 'SelectBox',
    props: {
        label: String,
        options: Array,
        modelValue: [String, Number]
    }

}
</script>

<style scoped>
.box {}

select {
    border-radius: 7px;
    background: #FFF;
    display: flex;
    width: 143px;
    height: 25px;
    padding: 0px 7px;
    justify-content: space-between;
    align-items: center;
    flex-shrink: 0;
}
</style>