<template>
  <!-- <router-link class="event-link"> -->
  <router-link
    class="event-link"
    :to="{ name: 'EventDetails', params: { id: people.id } }"
  >
    <div class="container">
      <div class="event-card">
        <div class="box">
          <br />
          <br />
          <br />
          <div class="content">
            <h4>{{ people.name }}<br />{{ people.surname }}</h4>

            <span>number of doses : {{ people.vaccine_status }}</span>
          </div>
        </div>
      </div>
    </div>
  </router-link>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    people: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
/* .event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #0a0a0a;
  margin-bottom: 18px;
  background-color: #a3fca2;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
.event-link {
  color: #0a0a0a;
  text-decoration: none;
} */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700;800&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  min-height: 100vh;
  background: #47516f;
}

body .container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 40px 0;
}

body .container .event-card {
  position: relative;
  min-width: 320px;
  height: 440px;
  box-shadow: inset 5px 5px 5px rgba(112, 112, 112, 0.2),
    inset -5px -5px 15px rgba(131, 131, 131, 0.1),
    5px 5px 15px rgba(0, 0, 0, 0.3), -5px -5px 15px rgba(255, 255, 255, 0.1);
  border-radius: 15px;
  margin: 30px;
  transition: 0.5s;
}

body .container .event-card .box {
  position: absolute;
  top: 20px;
  left: 20px;
  right: 20px;
  bottom: 20px;
  background: black;
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  transition: 0.5s;
}

body .container .event-card .box:hover {
  transform: translateY(-50px);
}

body .container .event-card .box:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 50%;
  height: 100%;
  background: rgba(255, 255, 255, 0.03);
}

body .container .event-card .box .content {
  padding: 20px;
}

body .container .event-card .box .content h4 {
  position: absolute;
  top: -10px;
  right: 30px;
  font-size: 3rem;
  color: white;
  text-align: left;
  text-indent: 50px;
}

body .container .event-card .box .content span {
  font-size: 1.8rem;
  color: #b3fbfc;
  z-index: 1;
  transition: 0.5s;
  margin-bottom: 15px;
  text-align: center;
}

body .container .event-card .box .content p {
  font-size: 1rem;
  font-weight: 300;
  color: black;
  z-index: 1;
  transition: 0.5s;
}

body .container .event-card .box .content a {
  position: relative;
  display: inline-block;
  padding: 8px 20px;
  background: black;
  border-radius: 5px;
  text-decoration: none;
  color: white;
  margin-top: 20px;
  box-shadow: 0 10px 20px black;
  transition: 0.5s;
}
body .container .event-card .box .content a:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.6);
  background: #fff;
  color: #000;
}
</style>
