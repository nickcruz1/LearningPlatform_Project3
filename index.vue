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
