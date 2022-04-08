<template>
    <div>
        <div class="container p-2">
            <div class="row">
                <div class="col-12">

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
            teacherCards: [
                {
                    title: 'It\'s a choise of quality for people with special needs',
                    text: 'I\'m a very strict person so require evedrything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                    name: 'Florence themes',
                    job: 'Multimedia Admin',
                    img: require('@/images/testimonial-avata-03.jpg')
                },
                {
                    title: 'High level of efficency and scientific teaching methods',
                    text: 'I am free to learn at my own space, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me.',
                    name: 'mina hollace',
                    job: 'Freelancer',
                    img: require('@/images/testimonial-avata-02.jpg')
                },
                {
                    title: 'High level of efficency and scientific teaching methods',
                    text: 'I am free to learn at my own space, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me.',
                    name: 'mina hollace',
                    job: 'Freelancer',
                    img: require('@/images/testimonial-avata-02.jpg')
                },
            ]
        }
    }
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
</style>
