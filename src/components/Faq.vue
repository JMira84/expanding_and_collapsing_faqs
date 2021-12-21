<template>
    <div class="faqs-wrapper">
        <div class="faq-wrapper" v-for="(cnt, index) in content" :key="index">
            <Header
            :title="cnt.title"
            :questionNumber="index + 1"
            :isOpen="cnt.isOpen"
            @headerAction="cnt.isOpen = !cnt.isOpen"/>
            <Body
            :text="cnt.text"
            :isOpen="cnt.isOpen"/>
        </div>
    </div>
</template>

<script>
import Header from '@/components/FaqHeader'
import Body from '@/components/FaqBody'
export default {
    props: {
        content: Array
    },
    components: {
        Header,
        Body
    }
}
</script>

<style lang="scss" scoped>
.faqs-wrapper {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 800px;
    .faq-wrapper {
        width: 100%;
        &:first-of-type {
            padding-bottom: 60px;
        }
    }
}
</style>