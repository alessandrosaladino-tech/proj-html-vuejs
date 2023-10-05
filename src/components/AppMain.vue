<script>
import AppServices from './AppServices.vue';
import AppBanner from './AppBanner.vue';
import AppCourse from './AppCourses.vue';
import AppFirstStep from './AppFirstStep.vue';
import AppEvents from './AppEvents.vue';
import AppNews from './AppNews.vue';
export default {
    name: "AppMain",
    components: {
        AppServices,
        AppBanner,
        AppCourse,
        AppFirstStep,
        AppEvents,
        AppNews,
    }
}
</script>

<template>
    <main class="main_section">
        <AppServices></AppServices>
        <AppBanner></AppBanner>
        <AppCourse></AppCourse>
        <AppFirstStep></AppFirstStep>
        <AppEvents></AppEvents>
        <AppNews></AppNews>
    </main>
</template>


<style lang="scss" scoped></style>