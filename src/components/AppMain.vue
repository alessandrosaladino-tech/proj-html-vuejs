<script>
import AppServices from './AppServices.vue';
import AppBanner from './AppBanner.vue';
import AppCourse from './AppCourses.vue';
import AppFirstStep from './AppFirstStep.vue';
export default {
    name: "AppMain",
    components: {
        AppServices,
        AppBanner,
        AppCourse,
        AppFirstStep,
    }
}
</script>

<template>
    <main class="main_section">
        <AppServices></AppServices>
        <AppBanner></AppBanner>
        <AppCourse></AppCourse>
        <AppFirstStep></AppFirstStep>
    </main>
</template>


<style lang="scss" scoped></style>