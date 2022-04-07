<template>
    <div>
        <div class="container p-2">
            <div class="row text-center mb-4">
                <div class="col-12">
                    <h6 class="text-uppercase fw-bold">maxcoach available courses</h6>
                    <h3 class="fw-bold">Acces <span>Smart Tutoring </span>Program For Benefits.</h3>
                </div>
            </div>
            <div class="row mb-4">
                <div class="col-12 d-flex justify-content-around">
                    <!-- CICLO LE CARD -->
                    <div class="card" v-for="(card, index) in smartCard" :key="index + 'c'">
                        <img :src="card.img" class="card-img-top" :alt="card.title">
                        <div class="card-body">
                            <h5 class="card-title fw-bold">{{card.title}}</h5>
                            <p class="card-text">{{card.paragraph}}</p>
                            <a href="#">{{card.start}} <i class="fas fa-long-arrow-alt-right"></i></a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="row mb-4 px-5">
                <div class="col-7 text-center position-relative">
                    <img :src="element.img" alt="backgound photo profile" class="position-absolute" :class="element.class" v-for="(element, index) in bgTutoring" :key="index + 'd'">
                    <img src="@/images/home-2-popup-video-poster.jpg" alt="popup photo poster" id="photo-poster" class="position-relative p-4">
                </div>
                <div class="col-5 p-4">
                    <h6 class="text-uppercase fw-bold">get started <span>effortlesly</span></h6>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SmartTutoring',
    data: function(){
        return{
            smartCard: [
                {
                    img: require('@/images/home-2-image-box-01.png'),
                    title: 'Customize Preferences',
                    paragraph: 'Learning are given the right to arrange and customize their study schedule and timetable based on preferences.',
                    start: 'Start here'
                },
                {
                    img: require('@/images/about-us-02-image-box-02.png'),
                    title: 'Cloud storage',
                    paragraph: 'You can store online lessons via online cloud or download to your device and revise lessons on the way.',
                    start: 'Get Free Quote '
                },
                {
                    img: require('@/images/home-2-image-box-03.png'),
                    title: 'Multimedia Channels',
                    paragraph: 'We provide study materials with varius formats: video, audio, sliades, doc, prints, book and applications.',
                    start: 'Start now'
                },
            ],
            bgTutoring: [
                {
                    img: require('@/images/maxcoach-shape-05-150x150.png'),
                    class: 'f-bg'
                },
                {
                    img: require('@/images/maxcoach-shape-07-150x150.png'),
                    class: 's-bg'
                },
                {
                    img: require('@/images/icon-youtube-play.png'),
                    class: 't-bg'
                },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
.col-12{
    h6{
        color: $ShadyLady;
    }
    h3{
        color: $GunPowder;
        span{
            color: $JungleGreen;
        }
    }
    .card{
        border: none;
        width: 18rem;
        img{
            width: 160px !important;
        }
        .card-body{
            .card-title{
                color: $GunPowder;
            }
            .card-text{
                color: $Edward;
            }
            a{
                text-decoration: none;
                color: $ShadyLady !important;
            }
        }
    }
}
.col-7{
    #photo-poster{
        z-index: 3;
        border-radius: 30px;
    }
    .f-bg{
        top: 10%;
        left: 0%;
    }
    .s-bg{
        bottom: -7%;
        right: 0%;
    }
    .t-bg{
        z-index: 5;
        top: 50%;
        left: 50%;
        transform: translate(-50% , -50%);
    }
}
.col-5{
    h6{
        color: $ShadyLady;
        span{
            color: $GunPowder;
        }
    }
}
</style>
