<template>
  <div class="container-wrapper">
    <div class="container">
      <div class="prose">
        <h1>Introduction</h1>
        <p>Are creatures of the cosmos intelligent beings bits of moving fluff a very small stage in a vast cosmic arena Tunguska event.</p>
      </div>
      <div class="sidebar">
        <div class="box">
          <div class="box-header">Actions</div>
          <ul class="box-menu">
            <li><a href="">Do a thing</a></li>
            <li><a href="">Register your bad self</a></li>
            <li><a href="">Hold the phone</a></li>
          </ul>
        </div>
        <div class="box">
          <div class="box-header">Related Stuff</div>
          <ul class="box-menu">
            <li><a href="">Just a link</a></li>
            <li><a href="">Another link</a></li>
          </ul>
        </div>
      </div>
      <div class="prose">
        <h1>Additional Information</h1>
        <p>Laws of physics Euclid courage of our questions? Permanence of the stars something incredible is waiting to be known two ghostly white figures in coveralls and helmets are soflty dancing tendrils of gossamer clouds hydrogen atoms laws of physics a very small stage in a vast cosmic arena extraordinary claims require extraordinary evidence encyclopaedia galactica brain is the seed of intelligence courage of our questions.</p>
      </div>
    </div>
  </div>
</template>

<style scoped> 
.box-menu li {
  margin: 0;
  padding: 0;
}

.container {
  display: grid;
  gap: 1.5em;
  margin: 1.5em;
  padding: 0 1.5em;
}

.prose * + * {
  margin-top: 20px;
}

.sidebar {
  display: inherit;
  gap: inherit;
}

.box {
  background: #dbe5ea;
  border-radius: 0.5em;
  overflow: hidden;
}
.box-header {
  background: #0F1C3F;
  color: white;
  font-size: 1.25em;
  padding: 1em;
}
.box-menu {
  list-style: none;
  padding: 0;
}
.box-menu a {
  background-color: rgba(255, 255, 255, .5);
  display: block;
  line-height: 1;
  padding: 1rem;
  text-decoration: none;
}

a {
  color: #456BD9;
}

.container-wrapper {
  contain: style layout inline-size;
}

@container (min-width: 600px) and (max-width: 900px) {
  .sidebar {
    grid-template-columns: 1fr 1fr;
  }
}

@container (min-width: 900px) {
  .container {
    grid-template-columns: 2fr 1fr;
  }
  .sidebar {
    grid-row: span 2;
    grid-auto-rows: min-content;
  }
}
</style>