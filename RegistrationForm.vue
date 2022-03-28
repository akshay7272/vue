<template>
{{form}}
    <form class="ff">
      <div>
       <label>Name</label>
      <input type="text"  v-model="form.name" />
      <br />
       <label>Father Name</label>
      <input type="text" v-model="form.father_name"/>
       <br />
       <label>Mother Name</label>
      <input type="text" v-model="form.mother_name" />
     
      <br />
      <label>Country</label>
      <select v-model="form.country">
        <option>India</option>
        <option>USA</option>
        <option>Germany</option>
      </select>
     <br />   <br /> 
     <label>Gender</label><br />  <br /> 
     <label for="male1">Male</label>
     <input type="radio"  v-model="form.gender"  id="male1" name="gender" value="male" />
     <label for="female1">Female</label>
     <input type="radio" id="female1"  v-model="form.gender"  name="gender" value="female" />
      <br />   <br />
      <h2>technologies</h2> 
      <label>Angular Js</label>
      <input type="checkbox" value="angular" v-model="form.techo" />
           <label>React Js</label>
      <input type="checkbox" value= "react" v-model="form.techo" />

           <label>Vue Js</label>
      <input type="checkbox" value="vue" v-model="form.techo" />
      <br />   <br />
    <button type="button"> Submit</button>



      </div>
     
    </form>
</template>
<script>
export default {
    name: 'RegistrationForm',
    data() {
      return {
        form: {
        name:'',
        father_name:'',
        mother_name:'',
        country:'',
        gender:'',
        techo:[],

        
      }
      }
    }
}
</script>

<style scoped>
form {
  margin:0 auto;
  align-items: center;
  text-align: center;
  width:100%;
  max-width:30%;
  background-color: rgb(19, 184, 196);
}

form.ff div {
  display: block;
}
</style>