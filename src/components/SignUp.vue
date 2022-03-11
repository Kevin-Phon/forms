<template>
  <form>
      <label>Email : </label>
      <input type="email" v-model="email">

      <label>Password : </label>
      <input type="password" v-model="password">

      <label for="">Roles : </label>  
      <select v-model="roles">
          <option value="unselect">None</option>
          <option value="developer">Web Developer</option>
          <option value="designer">Web Designer</option>
      </select>

        <!-- single checkbox (use true false)-->
      <div>
          <input type="checkbox" v-model="accept">
          <label>Terms and Conditions</label>
      </div>

        <!-- multiple checkbox (use array)-->
      <label>Select Names : </label>

      <div>
          <input type="checkbox" value="kevin" v-model="names">
          <label>Kevin</label>
      </div>
      <div>
          <input type="checkbox" value="kyawswa" v-model="names">
          <label>Kyaw Swa</label>
      </div>
      <div>
          <input type="checkbox" value="kayas" v-model="names">
          <label>KayAs</label>
      </div>
      <div>
          <input type="checkbox" value="yao" v-model="names">
          <label>Yao</label>
      </div>
  </form>
  <p>email - {{email}}</p>
  <p>password - {{password}}</p>
  <p>role - {{roles}}</p>
  <p>accept - {{accept}}</p>
  <p>{{names}}</p>
</template>

<script>
export default {
    data(){
        return{
            email : "@gmail.com",
            passwoed : "",
            roles : "unselect",
            accept : false,
            names : []
        }
    }
}
</script>

<style>
    form{
        max-width: 420px;
        margin: 30px auto;
        background: white;
        text-align: left;
        padding: 40px;
        border-radius: 10px;
    }
    label{
        color: #aaa;
        display: inline-block;
        margin: 25px 0 15px;
        font-size: 0.6em;
        text-transform: uppercase; 
        letter-spacing: 1px;
        font-weight: bold;
    }
    input,select{
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: none;
        border-bottom: 1px solid #ddd;
        color: #555;
    }
    input[type = "checkbox"] {
        display: inline-block;
        width: 16px;
        margin: 0 10px 0 0;
        position: relative;
        top: 2px;
    }
</style>