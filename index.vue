<!-- This will be a Big Learning Platform (Portfolio project: 
List of features:
- A Quiz
- Video tutorials/walkthrough of code
- Changing one set of code to another language/different style of code (modeled after Vue)
- Lots of Modals/Popups
- Include Vue Router
) -->
<template>
  <div id="app">
    <h1>{{ message }}</h1>
    
 <hr>
    <h2>Lessons (Click On A Lesson Below)</h2>
    
    <!-- **** Modal Section **** -->
    
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
