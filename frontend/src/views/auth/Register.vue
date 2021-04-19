<template>
  <div class="main">
            <!-- Sign up form -->
        <section class="signup">
            <div class="container">
                <div class="signup-content">
                    <div class="signup-form">
                        <h2 class="form-title">Sign up</h2>
                        <form method="POST" class="register-form" id="register-form" @submit.prevent="onSubmit">
                            <div class="form-group">
                                <label for="name"><i class="zmdi zmdi-account material-icons-name"></i></label>
                                <input type="text" name="fullName" id="fullName"  v-model="details.fullName" placeholder="Your Name"/>
                                
                            </div>
                            <div class="form-group">
                                <label for="email"><i class="zmdi zmdi-email"></i></label>
                                <input type="email" name="email" id="email" v-model="details.email"  placeholder="Your Email"/>
                              
                            </div>
                            <div class="form-group">
                                <label for="pass"><i class="zmdi zmdi-lock"></i></label>
                                <input type="password" name="password" id="password"  v-model="details.password" placeholder="Password"/>
                                
                            </div>
                            <div class="form-group form-button">
                                <input type="submit" name="register" class="form-submit" value="Register"/>
                            </div>
                        </form>
                    </div>
                    <div class="signup-image">
                        <figure><img src="../../assets/signup-image.jpg" alt="sing up image"></figure>
                        <router-link to="/login" class="signup-image-link">I am already member</router-link>
                    </div>
                </div>
            </div>
        </section>
  </div>

</template>

<script>

export default {

    data(){
        return{
            details: {
                fullName: null,
                email :null,
                password: null,
                
            }
        }
    },
    methods : {
        onSubmit(){
            let userRegister = {
                fullName: this.details.fullName,
                email : this.details.email,
                password: this.details.password
                                 }
                    console.log(userRegister);
                        this.fullName = '',
                        this.email = '',
                        this.password = '',
                console.log(userRegister);


        }
    }
};
</script>

<style scoped>
@import url('./css/auth.css');
</style>