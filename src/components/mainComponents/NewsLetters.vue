<template>
<div class="bg-white py-5">
    <div class="container p-2 bg-white">
        <div class="row text-center justify-content-center position-relative">
            <div class="col-12 align-items-center d-flex flex-column" >
                <h3 class="fw-bold mb-4">Subscribe <span class="fw-normal">Newsletters</span></h3>
                <p class="fw-bold mb-5">Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
                <div class="input-group mb-3">
                    <input type="text" class="form-control py-2" placeholder="Enter your email">
                    <button class="input-group-text text-white fw-bold py-2">Subscribe</button>
                </div>
                <img class="position-absolute my-left" src="@/images/maxcoach-shape-01.png" alt=".">
                <img class="position-absolute my-right" src="@/images/maxcoach-shape-02.png" alt=".">
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'NewsLetters'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
.col-12{
    h3{
        color: $GunPowder;
        span{
            color: $JungleGreen;
        }
    }
    p{
        color: $Edward;
    }
    .my-left,
    .my-right{
        bottom: 0%;
    }
    .my-left{
        left: 10%;
    }
    .my-right{
        right: 10%;
    }
    .input-group{
        width: 40%;
        input{
            background-color: $HintOfRed;
            border: none;
        }
        ::placeholder{
            color: $Edward;
        }
        button{
            width: 30%;
        }
    }
}
</style>
