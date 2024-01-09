<script>
import AppAboutMe from './AppAboutMe.vue';
import AppOnlineCourses from './AppOnlineCourses.vue';
import AppStoreBooks from './AppStoreBooks.vue';
export default {
    name: 'AppMain',
    data() {
        return {
            // creato un array per inserire i dati del corso attuali
            courseStatistics: [
                { name: 'Finished Season', data: '1.926' },
                { name: 'Satisfaction rate', data: '100%' },
                { name: 'Enrolled Learners', data: '3092+' },
                { name: 'Online Instructors', data: 200 }],
            // array per gli ultimi corsi disponibili
            latestCorses: [
                { id: 1, img: "../../../public/img-main-latest-courses/motivation-course-01-480x298.jpg", price: "$30.00", info: "How to be Successful:Create A Growth Mindset For Success", lessons: "3", students: "50" },

                { id: 2, img: "../../../public/img-main-latest-courses/motivation-course-02-480x298.jpg", alt: "picture teacher with students", price: "$30.00", info: "How to Build Confidence in Your Abilities", lessons: "1", students: "50" },

                { id: 3, img: "../../../public/img-main-latest-courses/motivation-course-03-480x298.jpg", alt: "picture another 2 man with pc", price: "$20.00", info: "Productivity Machine - Focus in a Distracted World", lessons: "5", students: "50" },

                { id: 4, img: "../../../public/img-main-latest-courses/motivation-course-04-480x298.jpg", alt: "man with pc", price: "$20.00", info: "Effective Time Management Mastery - Complete Guide", lessons: "18", students: "50" },

                { id: 5, img: "../../../public/img-main-latest-courses/motivation-course-05-480x298.jpg", alt: "picture alphaman drinking", price: "$25.99", info: "Body Language Secrets for Entrepreneurs", lessons: "18", students: "50" },

                { id: 6, img: "../../../public/img-main-latest-courses/motivation-course-06-480x298.jpg", alt: "picture alphaman calling", price: "$19.99", info: "Management Skills: The Science od Leadership", lessons: "17", students: "50" }],
            // array per la lista delle opportunità
            opportunityList: [
                'Help you understand yourself better',
                'Revealing mature tips',
                'Give the right advice',
                'Fascinating examples of alpha man'],
            // array dei libri da acquistare online
            booksShop: [
                { id: 1, img: '../../../public/img-main-store-book/product-book-11-400x400.jpg', info: "Alpha man by Maxcoach", info: "Alpha man by Maxcoach", price: "$29.00" },
                { id: 2, img: '../../../public/img-main-store-book/product-book-10-400x400.jpg', info: "Real man 4.0 by Maxcoach", price: "$39.00" },
            ],
            // array lista partnes
            brandPartnersList: [
                '../../../public/img-main-partners/client-logo-05-primary.png',
                '../../../public/img-main-partners/client-logo-06-primary.png',
                '../../../public/img-main-partners/client-logo-07-primary.png',
                '../../../public/img-main-partners/client-logo-08-primary.png',
                '../../../public/img-main-partners/client-logo-03-primary.png',
                '../../../public/img-main-partners/client-logo-02-primary.png'
            ]
        }
    },
    components: {
        AppAboutMe,
        AppOnlineCourses,
        AppStoreBooks
    }
}
</script>
<template>
    <main>
        <AppAboutMe />
        <AppOnlineCourses :latestCorses="latestCorses" />
        <AppStoreBooks :booksShop="booksShop" :opportunityList="opportunityList" :brandPartnersList="brandPartnersList" />
    </main>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

div.my_wrapper {
    @include container (width, margin);
    margin-bottom: 3rem;

    section.value-course {

        .value-date {
            color: $color-2
        }

        .value-info {
            font-size: .7rem;
        }

    }

}
</style>