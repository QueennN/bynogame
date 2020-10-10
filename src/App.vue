<template>
    <div>
        <by-navbar />
        <router-view />
        <by-footer />
    </div>
</template>

<script>
import nav from "./components/nav/nav";
import footer from "./components/footer/footer";
export default {
    components: {
        "by-footer": footer,
        "by-navbar": nav
    }
};
</script>

<style lang="scss">
$title: rgb(167, 82, 82);
$text: rgb(203, 207, 205);
$text-dark: rgb(59, 59, 59);

$bg-dark: rgb(58, 57, 57);
$bg-light: rgb(140, 143, 142);

.title {
    color: $title;
}
.text {
    color: $text;
}
.bg-dark {
    background-color: $bg-dark;
}
.text-dark {
    color: $text-dark;
}
.bg-light {
    background-color: $bg-light;
}
</style>
