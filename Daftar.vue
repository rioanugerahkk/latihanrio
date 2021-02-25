<template>
<div class="signup">
 <div class="content">
    <div class="wrapper">
       <div class="title">Buat Akun Anda</div>
            <form action="#">    
        <div class="field">
          <input type="text1" required>
          <label>Nama Depan</label>
        </div>
         <div class="field">
          <input type="text2" required>
          <label>Nama Belakang</label>
        </div>
        <div class="field">
          <input type="text" required>
          <label>Nama Pengguna</label>
        </div>
        <div class="field">
          <input type="password" required>
          <label>Masukan Password</label>
        </div>
        <div class="field">
          <input type="Password" required>
          <label>Masukan Ulang Password</label>
        </div>
        <div class="content">
          <div class="checkbox">
            <input type="checkbox" id="remember-me">
            <label for="remember-me">Remember me</label>
          </div>
           <div class="pass-link"><a href="#">Forgot password?</a></div>
        </div>
        <div class="field">
          <input type="submit" value="Daftar">
        </div>
   
      </form>
    </div>
 </div>  
</div>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700&display=swap');

.signup {
    display: flex;
    justify-content: center;
    margin-top: 50px;
}

.content {
    width: 70%;
}

.wrapper{
  width:800px;
  background:#fff;
  border-radius: 15px;
  box-shadow: 10px 15px 20px rgba(0,0,0,0.1);
}

.wrapper .title{
  font-size: 35px;
  font-weight: 600;
  text-align: center;
  line-height: 100px;
  color:black;
  user-select: none;
}
.wrapper form{
  padding:10px 30px 50px 30px;
  
}
.wrapper form .field{
  height:50px;
  width:100%;
  margin-top:20px;
  position: relative;
}
.wrapper form .field input{
  height:100%;
  width:50%;
  outline:none;
  font-size: 17px;
  padding-left: 20px;
  border:1px solid lightgray;
  border-radius: 25px;
  transition: all 0.3s ease;
  float: left;
}

.wrapper form .field input{
  height:100%;
  width:50%;
  outline:none;
  font-size: 17px;
  padding-left: 20px;
  border:1px solid lightgray;
  border-radius: 25px;
  transition: all 0.3s ease;
  float: left;
}

.wrapper form .field input:focus,
form .field input:valid{
  border-color: blue;
}
.wrapper form .field label{
  position:absolute;
  top:50%;
  left:20px;
  color:#999;
  font-weight: 400;
  font-size: 17px;
  pointer-events: none;
  transform:translateY(-50%);
  transition: all 0.3s ease;
}

form .field input:focus ~ label,
form .field input:valid ~ label{
  top:0%;
  font-size: 16px;
  color: rgb(0, 89, 255);
  background:#fff;
  transform:translateY(-50%);
}

form .content{
  display:flex;
  width:100%;
  height:50px;
  font-size: 16px;
  align-items:center;
  justify-content:space-between;
}

form .content .checkbox{
  display:flex;
  align-items:center;
  justify-content:center;
}

form .content input{
  width:15px;
  height:15px;
}

form .content label{
  color:#262626;
  user-select: none;
  padding-left:5px;
}

form .content .pass-link a{
  color: blue;
}

form .field input[type="submit"]{
  color:#fff;
  border:none;
  padding-left:0;
  margin-top:-10px;
  font-size: 20px;
  font-weight: 500;
  cursor: pointer;
  background:  rgb(0, 89, 255);
  transition:all 0.3s ease;
}

form .field input[type="submit"]:hover{
    background-color: rgb(42, 226, 42);
}


form .field input[type="submit"]:active{
  transform:scale(0.95);
}
form .signup-link{
  color:#262626;
  margin-top:20px;
  text-align: center;
}
form .pass-link a,
form .signup-link a{
  color: blue;
  text-decoration: none;
}

</style>
