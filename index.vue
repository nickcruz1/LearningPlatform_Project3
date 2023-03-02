<!-- This will be a Big Learning Platform (Portfolio project: 
List of features:
- A Quiz
- Video tutorials/walkthrough of code
- Changing one set of code to another language/different style of code (modeled after Vue)
- Lots of Modals/Popups
- Include Vue Router
) -->
<template>
   <div class="titleContainer">
      <h1>&#128161; {{ message }}</h1>
      
       <div class="rightTitleContainer">
        <div @click="logIn" class="logIn">&#128682; Log In</div>
        <div class="resources">&#128214; Resources</div>
      </div>
    </div>
    
        <label for="enterName">&#129485; Please Enter Your Name:</label>
      <input class="userName" type="text" />
      <label for="enterPassword">&#x1f92b; Please Enter Your Password:</label>
      <input type="password" />
      <button @click="loggedIn">&#9993; Log In</button>
    </div>
    
 <hr>
    <h2>Lessons (Click On A Lesson Below)</h2>
    
    <!-- **** Modal Section **** -->
    
    <div class="logInModal">
      <div class="logInModalInner">
        <h2>Log In</h2>
        <h4 @click="closeLogInModal">X</h4>
      </div>
    
    <!-- HTML Modal -->
    <div class="hModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>HTML Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>

   <!-- CSS Modal -->
    <div class="cModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>CSS Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>

   <!-- JS Modal -->
    <div class="jModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>JavaScript Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>
    
      <!-- Git Modal -->
    <div class="gModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>Git Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>
    
      <!-- SQL Modal -->
    <div class="sModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>SQL Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>
    
    
     <!-- Vue.js Modal -->
    <div class="vModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>Vue.js Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>
    
      <!-- Python Modal -->
    <div class="pModal">
      <div class="modalContainer">
      <button @click="closeModal">X</button>
      <h2>Python Lesson Plan </h2>
      <video height="50" width="auto"></video>
      <button>Learn More</button>
  </div>
    </div>
    
    <input type="text" id="myInput" @keyup="filterLessons" placeholder="Search for names.." title="Type in a name">

<ul id="myUL">
  <li><a @click="hModal" href="#">HTML</a></li>
  <li><a @click="cModal" href="#">CSS</a></li>

  <li><a @click="jModal" href="#">JavaScript</a></li>
  <li><a @click="gModal" href="#">Git</a></li>

  <li><a @click="sModal" href="#">SQL</a></li>
  <li><a @click="vModal" href="#">Vue.js</a></li>
  <li><a @click="pModal" href="#">Python</a></li>
</ul>
    
  </div>
</template>

 <script>
      export default {
        data() {
          return {
            message: "Learning Platform"
          };
        },
        methods: {
          logIn() {
      let logInModal = document.querySelector(".logInModal");

      logInModal.style.display = "block";
    },
     loggedIn() {
      let userName = document.querySelector(".userName");
      let logInModal = document.querySelector(".logInModal");

      alert("You are logged In!");

      document.querySelector(
        ".logIn"
      ).innerHTML = `<h2> Welcome ${userName.value}! &#128513;</h2>`;

      logInModal.style.display = "none";
    },
      closeLogInModal() {
      let logInModal = document.querySelector(".logInModal");

      logInModal.style.display = "none";
    },
          hModal() {
            let hModal = document.querySelector(".hModal");
            hModal.style.display = "block";
          },
           cModal() {
            let cModal = document.querySelector(".cModal");
            cModal.style.display = "block";
          },
          jModal() {
            let jModal = document.querySelector(".jModal");
            jModal.style.display = "block";
          },
          gModal() {
            let gModal = document.querySelector(".gModal");
            gModal.style.display = "block";
          },
          sModal() {
            let sModal = document.querySelector(".sModal");
            sModal.style.display = "block";
          },
          vModal() {
            let vModal = document.querySelector(".vModal");
            vModal.style.display = "block";
          },
          pModal() {
            let pModal = document.querySelector(".pModal");
            pModal.style.display = "block";
          },
          closeModal() {
            let hModal = document.querySelector(".hModal");
            let cModal = document.querySelector(".cModal");
            let jModal = document.querySelector(".jModal");
            let gModal = document.querySelector(".gModal");
            let sModal = document.querySelector(".sModal");
            let vModal = document.querySelector(".vModal");
            let pModal = document.querySelector(".pModal");
            
            hModal.style.display = "";
            cModal.style.display = "";
            jModal.style.display = "";
            gModal.style.display = "";
            sModal.style.display = "";
            vModal.style.display = "";
            pModal.style.display = "";
            
          },
          
           filterLessons() {
            
              var input, filter, ul, li, a, i, txtValue;
    
    input = document.getElementById("myInput");
    
    filter = input.value.toUpperCase();
    
    ul = document.getElementById("myUL");
    
    li = ul.getElementsByTagName("li");
    
    for (i = 0; i < li.length; i++) {
        a = li[i].getElementsByTagName("a")[0];
        txtValue = a.textContent || a.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
            li[i].style.display = "";
        } else {
            li[i].style.display = "none";
        }
    }
          }
        }
      };
    </script>
    
      <style lang="scss">
          * {
        box-sizing: border-box;
      }
      
      #app {
        margin-top: 10px;
      }
      
      button:hover {
        cursor: pointer;
      }

</style>
