<template>
    <div class="header-wrapper">
        <div class="header-content">
            <div class="icon-wrapper">
                <Icon class="question-icon" :icon="`question-${questionNumber}`"/>
            </div>
            <div class="title-wrapper">
                <span class="question-title">{{title}}</span>
            </div>
        </div>
        <div class="header-background-box" :class="{'change-color': isOpen}">
            <div @click="$emit('headerAction')">
                <Icon class="action-icon" :icon="boxIcon" :key="boxIcon"/>
            </div>
        </div>
    </div>
</template>

<script>
import Icon from '@/components/Icon'
export default {
    props: {
        title: String,
        questionNumber: Number,
        isOpen: Boolean
    },
    components: {
        Icon
    },
    computed: {
        boxIcon () {
            return this.isOpen ? 'close' : 'chevron'
        }
    }
}
</script>

<style lang="scss" scoped>
.header-wrapper {
    position: relative;
    height: 100px;
    .header-content {
        position: absolute;
        top: -12px;
        left: -40px;
        display: flex;
        width: 100%;
        height: 90%;
        .icon-wrapper {
            position: relative;
            min-width: 75px;
            background-color: #000;
            z-index: 1;
            ::v-deep svg {
                position: absolute;
                top: -40px;
                left: 10px;
            }
        }
        .title-wrapper {
            display: flex;
            align-items: center;
            width: 100%;
            padding: 20px;
            border: 4px solid #000;
            background-color: #fff;
            z-index: 1;
            .question-title {
                font-size: 1.1rem;
                font-weight: 800;
            }
        }
    }

    .header-background-box {
        width: 100%;
        height: 100px;
        background-color: #F0F0F0;
        transition: background .9s ease-out;
        ::v-deep svg {
            position: absolute;
            right: 11px;
            top: 15px;
            cursor: pointer;
        }
        &.change-color {
            background-color: #FFDD00;
            transition: background .3s ease-in;
        }
    }
}
</style>