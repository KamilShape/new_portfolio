<template>
  <section class='contactSection'>
    <h1 class='contactSection_header' data-aos="zoom-in-up" data-aos-duration="1000">CONTACT</h1>

    <div class='contactSection_container'>
      <section class='contactSection_contacts'>
        <p class='contactSection_contact'><i class="fas fa-phone contactSection_icon"> </i>Phone: 609 105 289</p>
        <p class='contactSection_contact'><i class="fas fa-envelope contactSection_icon"> </i>E-mail: kamil.linstedt@gmail.com</p>
        <p class='contactSection_contact'><i class="fas fa-home contactSection_icon"></i>Location: Gdańsk, Poland</p>
      </section>
      <h1 class='contactSection_header contactSection_header-form' >Questions? Send message :)</h1>
      <section class="contactSection_form" >
        <div class="contactSection_inputs">
          <input type="text" placeholder='Name' class="contactSection_input">
          <input type="text" placeholder='E-mail' class="contactSection_input">
        </div>
          <textarea placeholder='Type your message' class='contactSection_message' ></textarea>
        <button class="contactSection_button">Send</button>
      </section>
    </div>

    <div class="contactSection_socialMedia" >
      <a href='https://github.com/KamilShape' class="contactSection_icon"><i class="fab fa-github"></i></a>
      <a href='https://www.linkedin.com/in/kamil-linstedt-506737201/' class="contactSection_icon"><i class="fab fa-linkedin"></i></a>
    </div>

    <footer class='contactSection_footer'>
      <p class="contactSection_name">Kamil Linstedt ©2021</p>
    </footer>
  </section>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style lang='scss'>

.contactSection {
  min-height: 1000px;
  height: 100vh;
  position: relative;
  background-color: rgb(51, 153, 255);

&_header {
  position: relative;
  top: 30px;
  font-size: 1.4rem;
  padding: 10px;
  text-align: center;
}
&_header-form {
  position: relative;
  font-size: 1.3rem;
  padding: 10px;
  text-align: center;
}
&_container{
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  width: 80%;
}
&_contacts{
 display: flex;
 flex-direction: column;
 margin: 20px auto;
 box-sizing: border-box;
}
&_contact{
  font-size: 0.8rem;
  transform: translateY(50%);
  margin-bottom: 10px;
  width: 100%;
}
&_icon{
  font-size: 2rem;
  margin-right: 15px;
  text-decoration: none;
  color: black
}
&_form{
  margin: 30px auto;
 width: 100%;
 padding: 20px;
 box-sizing: border-box;
}
&_inputs{
  display: flex;
  flex-direction: column;
}
&_input{
  font-size: 0.8rem;
  margin: 5px;
  width: 100%;
  box-sizing: border-box;
  padding: 10px;
  background-color: rgb(152,221,252);
  outline: none;
  border: none;
  border-radius: 20px;
}

&_message{
  font-size: 0.8rem;
  display: block; 
  width: 100%;
  height: 150px;
  box-sizing: border-box;
  background-color: rgb(152,221,252);
  padding: 10px;
  margin: 5px;
  border: none;
  border-radius: 20px;
  resize: none;  
  outline: none;
}
&_button{
  display: block;
  font-size: 0.8rem;
  padding: 10px;
  margin: 15px auto;
  border-radius: 10px 0 10px 0;
  outline: none;
  transition: 0.5s;
  border: none;
  background-color: rgb(152,221,252);
}
&_button:hover{
  cursor:pointer;
  border-radius: 0 10px 0 10px;
}

&_socialMedia{
  display: flex;
  justify-content: space-evenly;
  margin: 0 auto;
  width: 20%;
  font-size: 2rem;
}
&_footer{
  position: absolute;
  height: 10%;
  width: 100%;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  background-color: rgb(152,221,252);
}
&_name{
  position: absolute;
  font-size: 1rem;
  bottom: 50%;
  left: 50%;
  transform: translate(-50%,50%);
}
}
@media (min-width: 414px) {
  .contactSection{
    &_header{
    font-size: 1.5rem;
    }
    &_contact{
      font-size: 0.85rem;
    }
    &_icon{
      font-size: 2.2rem;
    } 
    &_form {
      width: 85%;
    }
    &_input{
      font-size: 0.85rem;
    }
    &_message{
      font-size: 0.85rem;
    }
    &_button{
      font-size: 0.85rem;
    }
    &_name{
      font-size: 1.05rem;
    }
  }
} 
  
@media (min-width: 768px) {
  .contactSection {
    &_header{
      font-size: 1.7rem;
    }
    &_contact {
      font-size: 0.9rem;
    }
    &_form {
      width: 70%;
    }
    &_input{
      font-size: 0.9rem;
    }
    &_message{
      font-size: 0.9rem;
    }
    &_button{
      font-size: 0.9rem;
    }
    &_name{
      font-size: 1.1rem;
    }
  }
}
@media (min-width: 1024px) {
  .contactSection{
    &_header{
      font-size: 1.9rem;
    }
    &_contact{
      font-size: 0.95rem;
    }
      &_icon{
      font-size: 2.4rem;
    } 
    &_form {
      width: 55%;
    }
    &_input{
      font-size: 0.95rem;
    }
    &_message{
      font-size: 0.95rem;
    }
    &_button{
      font-size: 0.95rem;
    }
    &_name{
      font-size: 1.15rem;
    }
  }
}
@media (min-width: 1280px){
  .contactSection {
    &_header{
      font-size: 2.1rem;
    }
    &_contact {
      font-size: 1rem;
    }
    &_form {
      width: 50%;
    }
    &_input{
      font-size: 1rem;
    }
    &_message{
      font-size: 1rem;
    }
    &_button{
      font-size: 1rem;
    }
      &_name{
      font-size: 1.2rem;
    }
  }
}
@media (min-width: 1440px) {
  .contactSection {
    &_header{
      font-size: 2.3rem;
    }
    &_contact {
      font-size: 1.05rem;
    }
    &_icon{
      font-size: 2.4rem;
    } 
    &_form {
      width: 45%;
    }
    &_input{
      font-size: 1.05rem;
    }
    &_message{
      font-size: 1.05rem;
    }
    &_button{
      font-size: 1.05rem;
    }
    &_name{
      font-size: 1.25rem;
    }
  }
}
</style>

 

