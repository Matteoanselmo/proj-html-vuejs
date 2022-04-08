<template>
    <div>
        <div class="p-2">
            <div class="row text-center my-5 p-0">
                <div class="col-12">
                    <h6 class="text-uppercase fw-bold">great awords about maxcoach</h6>
                    <h3 class="fw-bold">Our <span>Top Learner's </span>verbatim</h3>
                </div>
            </div>
            <div class="row g-3 justify-content-evenly">
                <div class="col-3 bg-white rounded teacher-wrapper p-4 mb-4 " v-for="(teacher, index) in teacherCards" :key="index + 'f'" :class="(index === elementActive) ? ' active ' : ''" @click="elementActive = index">
                    <h5 class="fw-bold mb-3">{{teacher.title}}</h5>
                    <p class="fw-bold">{{teacher.text}}</p>
                    <div class="d-flex" id="teacher-min-card">
                        <img :src="teacher.img" :alt="teacher.job" class="rounded-circle me-3">
                        <div>
                            <p class="text-uppercase mb-2 fw-bold fs-7">{{teacher.name}}</p>
                            <p>/ {{teacher.job}}</p>
                        </div>
                    </div>
                </div>
                <div class="col-12 text-center selected-teacher-circle">
                    <i class="fas fa-circle me-3" v-for="(teacher, index) in teacherCards" :key="index + 'g'" :class="(index === elementActive) ? ' active ' : ''" @click="elementActive = index"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TopLearners',
    data: function(){
        return{
            elementActive : 1,
            teacherCards: [
                {
                    title: 'It\'s a choise of quality for people with special needs',
                    text: 'I\'m a very strict person so require evedrything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                    name: 'Florence themes',
                    job: 'Multimedia Admin',
                    img: require('@/images/testimonial-avata-03.jpg'),
                    clicked: false
                },
                {
                    title: 'High level of efficency and scientific teaching methods',
                    text: 'I am free to learn at my own space, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me.',
                    name: 'mina hollace',
                    job: 'Freelancer',
                    img: require('@/images/testimonial-avata-02.jpg'),
                    clicked: true
                },
                {
                    title: 'Professional team of specialists and passionate mentors at reach',
                    text: 'I need to get certification for English proficiency and MaxCoaching is my best choice. Their tutors are smart and professional when dealing with students.',
                    name: 'madley pondor',
                    job: 'IT Specialist',
                    img: require('@/images/testimonial-avata-04.jpg'),
                    clicked: false
                },
            ]
        }
    },
    // methods: {
    //     showTeacherCard(){
    //         this.teacherCards.clicked = !this.teacherCards.clicked;
    //     }
    // }
    
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
}
.selected-teacher-circle{
    i{
        cursor: pointer;
        filter: opacity(50%);
    }
}
.teacher-wrapper{
    cursor: pointer;
    filter: opacity(50%);
    #teacher-min-card{
        img{
            height: 75px;
            width: 75px;
        }
    }
    h5{
        color: $GunPowder
    }
    p{
        color: $Edward;
    }
    #teacher-min-card{
        p:first-child{
            color: $GunPowder;
        }
    }
}
.teacher-wrapper.active{
    filter: opacity(100);
}
.selected-teacher-circle{
    i.active{
        filter: opacity(100);
    }
}
</style>
