<script>
import AppAboutMe from './AppAboutMe.vue';
import AppOnlineCourses from './AppOnlineCourses.vue';
import AppStoreBooks from './AppStoreBooks.vue';
import AppRealStoies from './AppRealStoies.vue';
export default {
    name: 'AppMain',
    data() {
        return {
            // creato un array per inserire i dati del corso attuali
            courseStatistics: [
                { id: 1, name: 'Finished Season', data: '1.926' },
                { id: 2, name: 'Satisfaction rate', data: '100%' },
                { id: 3, name: 'Enrolled Learners', data: '3092+' },
                { id: 4, name: 'Online Instructors', data: 200 }],
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
                '../../../public/img-main-partners/client-logo-04-primary.png',
                '../../../public/img-main-partners/client-logo-03-primary.png',
                '../../../public/img-main-partners/client-logo-02-primary.png'
            ],
            // array testimonials
            testimonials: [
                { id: 1, name: 'Mina Hollace', work: 'Freelancer', info: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.', img: '../../../public/img-main-real-stories/testimonial-avata-02.jpg' },

                { id: 2, name: 'Karl Hainze', work: 'Calientacamas', info: 'Translated from the Spanish, the "warms bed". These are people who are paid to slip into other people’s beds and make the sheets warm before they decide to go to bed.', img: '../../../public/img-main-real-stories/testimonial-avata-03.jpg' },

                { id: 3, name: 'Joseph Onion', work: 'No Work', info: 'No work but i want to be a AlphaMan', img: '../../../public/img-main-real-stories/testimonial-avata-01.jpg' },

                { id: 4, name: 'Mark Landers', work: 'Water Slide Tester', info: 'Water Slide Tester" involves sliding down water slides to assess safety and enjoyment, ensuring water park visitors have a thrilling yet secure experience. It combines fun with responsibility to maintain quality standards', img: '../../../public/img-main-real-stories/testimonial-avata-04.jpg' }
            ]
        }
    },
    components: {
        AppAboutMe,
        AppOnlineCourses,
        AppStoreBooks,
        AppRealStoies
    }
}
</script>
<template>
    <main>
        <AppAboutMe />
        <AppOnlineCourses :latestCorses="latestCorses" />
        <AppStoreBooks :booksShop="booksShop" :opportunityList="opportunityList" :brandPartnersList="brandPartnersList" />
        <AppRealStoies :testimonials="testimonials" />
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