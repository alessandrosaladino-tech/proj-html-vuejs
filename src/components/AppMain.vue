<script>
import AppServices from './AppServices.vue';
import AppBanner from './AppBanner.vue';
import AppCourse from './AppCourses.vue';
export default {
    name: "AppMain",
    components: {
        AppServices,
        AppBanner,
        AppCourse
    }
}
</script>

<template>
    <main class="main_section">
        <AppServices></AppServices>
        <AppBanner></AppBanner>
        <AppCourse></AppCourse>
    </main>
</template>


<style lang="scss" scoped></style>