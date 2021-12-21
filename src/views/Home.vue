<template>
    <div class="container">
        <Faq :content="faqContent"/>
    </div>
</template>

<script>
import Faq from '@/components/Faq'
export default {
    components: {
        Faq
    },
    data () {
        return {
            faqContent: [
                {
                    title: "What are the most commonly used Directives in Vue.js? What do you understand by the conditional directives in Vue.js?",
                    text: 'Bacon ipsum dolor amet jowl filet mignon biltong shoulder shank salami prosciutto meatloaf jerky. Andouille leberkas beef ribs tail rump strip steak, turkey drumstick flank shoulder. Filet mignon tri-tip ham hock, cow sirloin tail shoulder cupim landjaeger drumstick capicola ball tip jerky tongue pork loin. Brisket kielbasa prosciutto hamburger. Ribeye ham hock short ribs capicola strip steak turducken, jerky sirloin.',
                    isOpen: false
                },
                {
                    title: 'Do you provide a certificate of completion?',
                    text: 'Bacon ipsum dolor amet jowl filet mignon biltong shoulder shank salami prosciutto meatloaf jerky. Andouille leberkas beef ribs tail rump strip steak, turkey drumstick flank shoulder. Filet mignon tri-tip ham hock, cow sirloin tail shoulder cupim landjaeger drumstick capicola ball tip jerky tongue pork loin. Brisket kielbasa prosciutto hamburger. Ribeye ham hock short ribs capicola strip steak turducken, jerky sirloin.',
                    isOpen: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.container {
    display: flex;
	justify-content: center;
    padding: 110px 30px 30px 30px;
}
</style>