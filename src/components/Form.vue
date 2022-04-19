<template>
    <form @submit="onSubmit" class="add-form">
    <div class="form-control">
      <label>First Name</label>
      <input type="text" v-model="firstName" name="firstName" placeholder="Your First Nme" />
    </div>
    <div class="form-control">
      <label>Last Name</label>
      <input
        type="text"
        v-model="lastName"
        name="lastName"
        placeholder="Your Last Name"
      />
    </div>
    <div class="form-control">
      <label>E-mail</label>
      <input
        type="email"
        v-model="email"
        name="email"
        placeholder="Your E-Mail"
      />
    </div>
    

    <input type="submit" value="Send" class="btn btn-block" />
  </form>
</template>
<script>
export default{
    name: 'Form',
    data() {
        return {
            firstName:'',
            lastName:'',
            email:'',
            
        }
    },
    methods: {
        onSubmit(e){
            e.preventDefault()
            if(!this.firstName || !this.lastName || !this.email){
                alert('Please Fill Out the Form Completely')
                }
            else {
                alert('Hello at Hokify!')
            }
            //ich wollte diese Info in einer Liste auf eine andere Seite darstellen
            const newInfo = {
                firstName: this.firstName,
                lastName: this.lastName,
                email: this.email
            }
            

            this.firstName=''
            this.lastName=''
            this.email=''
    },
}
}
</script>
<style scoped>
.add-form {
  margin-bottom: 40px;
}
.form-control {
  margin: 20px 0;
}
.form-control label {
  display: block;
}
.form-control input {
  width: 100%;
  height: 40px;
  margin: 5px;
  padding: 3px 7px;
  font-size: 17px;
}
.form-control-check {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.form-control-check label {
  flex: 1;
}
.form-control-check input {
  flex: 2;
  height: 20px;
}
</style>