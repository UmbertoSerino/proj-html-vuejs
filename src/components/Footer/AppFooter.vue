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
        <section class="my_wrapper">
            <div class="row">
                <div class="col-6" v-for="info in Address" :key="info">
                    <h1>Address</h1>
                    <p>
                        {{ info.street }}
                    </p>
                    <p>
                        {{ info.phoneNumber }} ( {{ info.workTime }} )
                    </p>
                    <p>
                        {{ info.mail }}
                    </p>
                </div>
            </div>
        </section>
    </footer>
</template>
<style lang="scss">
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

footer {
    background-color: $color-9;
    height: 500px;

    section.my_wrapper {
        @include container (width, margin);
    }
}
</style>