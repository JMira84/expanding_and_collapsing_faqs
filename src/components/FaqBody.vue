<template>
    <div class="body-wrapper" :class="{open: isOpen}">
        <p class="body-text" :class="{show: isOpen}">{{text}}</p>
    </div>
</template>

<script>
export default {
    props: {
        text: String,
        isOpen: Boolean
    }
}
</script>

<style lang="scss" scoped>
.body-wrapper {
    max-height: 0;
    background-color: #FFDD00;
    transition: max-height .5s ease-out;
    .body-text {
        padding: 0 60px 40px 60px;
        font-size: .9rem;
        line-height: 2;
        opacity: 0;
        transition: opacity .4s ease-out;
        &.show {
            opacity: 100;
            transition: opacity .8s ease-in;
        }
    }
    &.open {
        max-height: 500px;
        transition: max-height .5s ease-in;
    }
}
</style>