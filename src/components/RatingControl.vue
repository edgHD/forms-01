<template>
    <ul>
        <li :class="{ active: modelValue === 'poor' }"><button type="button" @click="activate('poor')">Poor</button>
        </li>
        <li :class="{ active: modelValue === 'average' }"><button type="button"
                @click="activate('average')">Average</button></li>
        <li :class="{ active: modelValue === 'great' }"><button type="button" @click="activate('great')">Great</button>
        </li>
    </ul>
</template>

<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue'],
    // data() {
    //     return {
    //         activeOption: this.modelValue
    //     };
    // },
    // computed: {
    //     activeOption() {
    //         return this.modelValue;
    //     }
    // }
    methods: {
        activate(option) {
            this.$emit('update:modelValue', option);
        }
    }
};
</script>

<style scoped>
.active {
    border-color: #ae00ff;
}

.active button {
    color: #ae00ff;
}

ul {
    list-style-type: none;
    padding: 0;
    display: flex;
    justify-content: space-evenly;
}

li {
    margin: 0 1rem;
    border: 1px solid #ccc;
    padding: 1rem;
    display: flex;
    align-items: center;
}

button {
    font: inherit;
    cursor: pointer;
    border: none;
    background-color: transparent;
    cursor: pointer;
}
</style>