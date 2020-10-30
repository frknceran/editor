<template>
    <div>
        <input type="text" ref="dayPicker"   placeholder="Day" :value="value.day" @input="updateDate()">
        <input type="text" ref="monthPicker" placeholder="Month" :value="value.month" @input="updateDate()">
        <input type="text" ref="yearPicker"  placeholder="Year" :value="value.year" @input="updateDate()">
    </div>
</template>

<script>
export default {
    props: ["value"],

    methods: {
        updateDate() {
            this.$emit("input", {
                day: this.$refs.dayPicker.value,
                month: this.$refs.monthPicker.value,
                year: this.$refs.yearPicker.value
            })
        }
    }
}
</script>
