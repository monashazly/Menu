<template>
  <div class="navv">
    <!-- Image and text -->
    <hr class="diss1" />
    <nav class=" navbar-light  container-fluid mt-4 mb-4 diss1">
      <div class="row coloror">
        <div style="display:inline " class="col-md-9 col-sm-8 ms-2 ps-5">
          <a class="navbar-brand" href="#">
            <img
              src="../assets/pngfind.com-napster-logo-png-5675066.png"
              width="30"
              height="30"
              class="d-inline-block align-top"
              alt=""
            />
            AL<b style="color:rgb(236, 164, 55)">MALL</b>
          </a>
        </div>
        <div
          class="col-md-1 fas fa-user user col-sm-1 ms-5 mt-2"
          style="width:50px;font-size:20px"
        ></div>
        <div
          class="col-md-1 fas fa-shopping-bag bag col-sm-1  mt-2 "
          style="width:50px;font-size:20px"
        ></div>
      </div>
    </nav>
    <hr class="diss1" />
    
    <div class="container  diss1 d-flex justify-content-center">
      <div class="row d-flex justify-content-center media1  " >
        <!-- First category  -->
        <div
          class="col-md-1 col-sm-1 lead m-auto text-center cat2 "
          style="font-size:15px"
          v-for="item8 in getArray2"
          :key="item8"
        >
          {{ item8 }}
        </div>
        <!-- second category  -->
        <div
          class="col-md-2 col-sm-2 lead m-auto text-center cat1"
          style="font-size:15px;font-weight:bold"
          v-for="item9 in getArray3"
          :key="item9"
        >
          {{ item9 }}
        </div>
        <!-- exceeds section -->
        <div class="col-1"  v-if="items.length > 5 || items2.length > 2">
          <div class="dropdown ">
            <div
              class="d-flex justify-content-center plus fas fa-plus ms-3 mt-2"
              id="dropdownMenuButton"
              data-toggle="dropdown"
              aria-expanded="false"
            ></div>
              
            <div
              class="dropdown-menu text-center menu1  "
              style="cursor:pointer"
              aria-labelledby="dropdownMenuButton"
            >
              <li class="dropdown-item" v-for="item4 in getArray" :key="item4">
                {{ item4 }}
              </li>
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr class="diss1" />
  </div>
  <!-- Mobile Display -->
  <div class="diss2 container-fluid">
    <nav class=" n navbar-light bg-light row">
      <div class="col-2 navbar">
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarTogglerDemo03"
          aria-controls="navbarTogglerDemo03"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
          <ul class="navbar-nav mr-auto mt-3 mt-lg-0">
            <li
              class="nav-item text-center cat1 mb-3 "
              v-for="item11 in getArray4"
              :key="item11"
            >
              {{ item11 }}
            </li>
            <li
              class="nav-item font-weight-bold text-center cat1 mb-3"
              v-for="item12 in getArray5"
              :key="item12"
            >
              {{ item12 }}
            </li>
          </ul>
        </div>
      </div>

      <div class="col-3 mt-2 me-5 logo ">
        <a class="navbar-brand sd" style="color:black;" href="#">
          <img
            src="../assets/pngfind.com-napster-logo-png-5675066.png"
            width="30"
            height="30"
            class="d-inline-block align-top"
            alt=""
          />
          AL <b style="color:rgb(236, 164, 55)">MALL</b>
        </a>
      </div>
      <!-- user -->
      <div
        class=" col-3 fas fa-user user mt-3 sd"
        style="width:50px;font-size:20px;color:rgb(236, 164, 55)"
      ></div>
      <!-- stock -->
      <div
        class=" col-3 fas fa-shopping-bag bag  mt-3 sd "
        style="width:50px;font-size:20px;color:rgb(236, 164, 55)"
      ></div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  props: {
    msg: String
  },
  data () {
    return {
      itemv: '',
      items: [
        'Men',
        'Women',
        'Sports',
        'Home',
        'Brands',
        'shoes',
        'Accessories'
      ],
      items2: ['Deals of the day', 'Ramadan Sale']
    }
  },
  computed: {
    getArray () {
      return this.items2
        .slice(2, this.items2.length)
        .concat(this.items.slice(5, this.items.length))
    },
    getArray2 () {
      return this.items.slice(0, 5)
    },
    getArray3 () {
      return this.items2.slice(0, 2)
    },
    getArray4 () {
      return this.items.slice(0, this.items.length)
    },
    getArray5 () {
      return this.items2.slice(0, this.items2.length)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lato&family=Oswald:wght@200;400&display=swap');
/* .flx{
  display: flex;
  justify-content:space-between;
} */
/* .flx2{
  margin: auto;
}  */
/* .user{
  margin-left: 300px;
}*/
.bag {
  margin-left: 0;
}
.coloror {
  color: rgb(236, 164, 55);
  overflow: hidden;
}
.boldd {
  font-family: 'Oswald', sans-serif;
  font-weight: bold;
}
.flxx {
  text-align: center;
  /* margin-left: 10% ; */
}
.plus {
  width: 25px;
  text-align: center;
  height: 15px;
  font-size: 13px;
  overflow: hidden;
}
.plus:hover {
  cursor: pointer;
  border: 1px solid;
  background: rgb(236, 164, 55);
  border-radius: 15px;
  border-style: none;
  animation: tada;
  animation-duration: 2s;
}
.menu1 {
  border: 1px solid rgb(236, 164, 55);
  margin-right: 60px;
  margin-top: 7px;
  /* background:rgb(236, 164, 55) ; */
}
.user {
  margin-left: 100px;
}
.user:hover {
  cursor: pointer;
  animation: heartBeat;
  animation-duration: 0.5s;
}
.bag:hover {
  cursor: pointer;
  animation: heartBeat;
  animation-duration: 0.5s;
}

.cat1:hover {
  cursor: pointer;
  background: rgb(236, 164, 55);
  animation: pulse;
  animation-duration: 1s;
  border: 1px solid;
  color: white;
  border-radius: 10px;
  border-style: none;
}
.cat2:hover{
  cursor: pointer;
    animation: pulse;
  animation-duration: 1s;
  font-weight: bold;
  font-size: 15px;

}


@media screen and (max-width: 575px) {
  .diss1 {
    display: none !important ;
  }
}
@media screen and (min-width: 575px) {
  .diss2 {
    display: none !important ;
  }
}
@media screen and (max-width: 375px) {
  .user{
    margin-left: 50px;
  }
}
@media screen and (min-device-width: 280px) and (max-device-width: 414px) { 
    .user{
    margin-left: 10px;
    }
    .sd{
      font-size: 15px;
      margin-top: 5px;
    }
}
</style>
