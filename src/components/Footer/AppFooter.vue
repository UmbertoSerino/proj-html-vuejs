<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            Address: [
                { street: '382 NE 191st St # 87394 Miami, FL 33179-3899', phoneNumber: '+1(305)547-9909', workTime: '9am - 5pm EST, Monday - Friday', mail: 'support@maxcoach.com' }
            ],
            explore: ['Start here', 'Blog', 'About us', 'Success story', 'Courses', 'Contact us'],
            information: ['Membership', 'Purchase guide', 'Privacy policy', 'Terms of service']
        }
    },
}
</script>
<template>
    <footer class="">
        <section class="my_wrapper text-white pt-5 pb-5">
            <div class="row">
                <div class="col-6" v-for="info in Address" :key="info">
                    <h1 class="fs-5 mb-4">Address</h1>
                    <p>
                        {{ info.street }}
                    </p>
                    <p>
                        {{ info.phoneNumber }} ( {{ info.workTime }} )
                    </p>
                    <p>
                        {{ info.mail }}
                    </p>
                    <div class="reference-footer">
                        <!-- icon per l'indirizzamento ai profili social -->
                        <a href="https://twitter.com/?lang=it"><i class="fa-brands fa-twitter"></i></a>
                        <a href="https://www.facebook.com/?locale=it_IT"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="https://www.instagram.com/"><i class="fa-brands fa-instagram"></i></a>
                        <a href="https://www.linkedin.com/"><i class="fa-brands fa-linkedin"></i></a>
                    </div>
                </div>
                <div class="col-md-3">
                    <h1 h1 class="fs-5">Explore</h1>
                    <div class="d-flex flex-column flex-wrap explore">
                        <div v-for="explore in explore" :key="explore">
                            <ul class="p-0">
                                <li>
                                    {{ explore }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-3">
                    <h1 class="fs-5">Information</h1>
                    <div v-for="info in information " :key="info">
                        <div>
                            <ul class="p-0">
                                <li>
                                    {{ info }}
                                </li>
                            </ul>
                        </div>

                    </div>
                </div>
            </div>
        </section>
        <section class="copryright">
            <p class="m-0 py-5 text-center">2020 Maxcoach. All Right Reserved</p>
            <a class="page-scroll-up">
                <i class="fa-solid fa-arrow-up"></i>
            </a>
        </section>
    </footer>
</template>
<style lang="scss">
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

footer {
    background-color: $color-9;

    div.explore {
        height: 150px
    }

    section.my_wrapper {
        @include container (width, margin);
    }

    p,
    li {
        color: rgb(160, 160, 160);
        font-weight: 700;
        font-size: .9rem
    }

    a.page-scroll-up {
        background-color: $color-2;
        color: white;
        position: fixed;
        right: 30px;
        bottom: 60px;
        z-index: 1;
        display: block;
        padding: 0;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        text-align: center;
        font-size: 25px;
        line-height: 60px;
        cursor: pointer;
    }

    div.reference-footer {

        a {
            margin-right: 2rem;
            font-size: 1.7rem;
            color: $color-7;
        }
    }
}
</style>