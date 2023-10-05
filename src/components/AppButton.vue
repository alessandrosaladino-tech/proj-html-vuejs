<script>
export default {
    name: "AppButton",
    data() {
        return {

        }
    }
}
</script>

<template>
    <button class="site_button">
        <slot></slot>

    </button>
</template>


<style lang="scss" scoped>

.site_button {
    width: 180px;
    height: 50px;
    padding: 4px;
    border-radius: 5px;
    font-weight: bold;

}

</style>