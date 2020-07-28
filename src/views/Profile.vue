<template>
  <div class="profile">
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-lg-3">
                    <div class="media text-left">
                        <img src="../assets/profile.jpeg" class="user-pic mr-3" alt="yudha">
                        <div class="media-body">
                            <h5 class="mt-0">{{firstName}} {{lastName}}</h5>
                            <p>{{textInfo}}</p>
                        </div>
                    </div>
              </div>
          </div>
      </div>
  </div>
</template>
<script>

    import 'bootstrap/dist/css/bootstrap.css'

    export default {
        name: 'Profile',
        data: function (){
            return {
                firstName : 'willie',
                lastName : 'yudha',
                textInfo : 'Baru belajar vue.js lur hehe :D'
            }
        },
        components: {

        }
    }
</script>
<style scoped>
    .user-pic{
        border-radius: 200%;
        height: 80px;
        width: 80px;
    }
</style>
