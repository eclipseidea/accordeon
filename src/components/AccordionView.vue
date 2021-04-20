<template>
  <div class="container">
    <div class="oranges-menu">
      <div :class="['oranges-tub',{'active_fruit': fruit === 'orange'}]">
        Апельсини
      </div>
      <div class= "oranges-countries">
        <div class="tur">
          <div :class="['turkish',{'active_fruit': country === 'turkish'}]">
            Турція
          </div>
          <p @click="click(1)"
             :class="['tur',{'active_link': orange_turkish_big}]">
            великі
          </p>
          <p @click="click(2)"
             :class="['tur',{'active_link': orange_turkish_middle}]" >
            середні
          </p>
          <p @click="click(3)"
             :class="['tur',{'active_link': orange_turkish_small}]">
            маленькі
          </p>
        </div>
        <div class="sp">
          <div  :class="['spain',{'active_fruit': country === 'spain'}]">
            Іспанія
          </div>
          <p @click="click(4)"
             :class="['spa-in',{'active_link': orange_spain_big}]">
            великі
          </p>
          <p @click="click(5)"
             :class="['spa-in',{'active_link': orange_spain_middle}]">
            середні
          </p>
        </div>
        <div class="tu">
          <div :class="['tunis',{'active_fruit': country === 'tunis'}]">
            Туніс
          </div>
          <p @click="click(6)"
             :class="['tun',{'active_link': orange_tunis_middle}]">
            середні
          </p>
          <p @click="click(7)"
             :class="['tun',{'active_link': orange_tunis_small}]">
            маленькі
          </p>
        </div>
      </div>
    </div>

    <div class="apples-menu">
      <div :class="['apples-tub',{'active_fruit': fruit === 'apple'}]">
        Яблука
      </div>
      <div class="apples-countries">
        <div class="ua">
          <div :class="['ukraine',{'active_fruit': country === 'ukraine'}]">
            Украіна
          </div>
          <p @click="click(8)"
             :class="['uah',{'active_link': apple_ukraine_golden}]">
            голден
          </p>
          <p @click="click(9)"
             :class="['uah',{'active_link': apple_ukraine_gala}]">
            гала
          </p>
        </div>
        <div class="pl">
          <div class=""
               :class="['poland',{'active_fruit': country === 'poland'}]">
            Польща
          </div>
          <p @click="click(10)"
             :class="['pl',{'active_link': apple_poland_golden}]">
            голден
          </p>
          <p @click="click(11)"
             :class="['pl',{'active_link': apple_poland_kalvin}]">
            кальвін
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "AccordionView",

    data() {
      return {
        fruit:null,
        country:null,
        active_element: null,
      }
    },

    computed: {

      orange_turkish_big() {
        return this.active_element === "orange_turkish_big"
      },

      orange_turkish_middle() {
        return this.active_element === "orange_turkish_middle"
      },

      orange_turkish_small() {
        return this.active_element === "orange_turkish_small"
      },

      orange_spain_big () {
        return this.active_element === "orange_spain_big"
      },

      orange_spain_middle () {
        return this.active_element === "orange_spain_middle"
      },

      orange_tunis_middle() {
        return this.active_element === "orange_tunis_middle"
      },

      orange_tunis_small() {
        return this.active_element === "orange_tunis_small"
      },

      apple_ukraine_golden() {
        return this.active_element === "apple_ukraine_golden"
      },

      apple_ukraine_gala() {
        return this.active_element === "apple_ukraine_gala"
      },

      apple_poland_golden() {
        return this.active_element === "apple_poland_golden"
      },

      apple_poland_kalvin() {
        return this.active_element === "apple_poland_kalvin"
      }
    },


    methods: {

      click(value) {
        switch (value) {
          case 1:
            this.fruit = "orange"
            this.country = "turkish"
            this.active_element = "orange_turkish_big"
            break;

          case 2:
            this.fruit = "orange"
            this.country = "turkish"
            this.active_element = "orange_turkish_middle"
            break;

          case 3:
            this.fruit = "orange"
            this.country = "turkish"
            this.active_element = "orange_turkish_small"
            break;

          case 4:
            this.fruit = "orange"
            this.country = "spain"
            this.active_element = "orange_spain_big"
            break;

          case 5:
            this.fruit = "orange"
            this.country = "spain"
            this.active_element = "orange_spain_middle"
            break;

          case 6:
            this.fruit = "orange"
            this.country="tunis"
            this.active_element = "orange_tunis_middle"
            break;

          case 7:
            this.fruit = "orange"
            this.country="tunis"
            this.active_element = "orange_tunis_small"
            break;

          case 8:
            this.fruit = "apple"
            this.country="ukraine"
            this.active_element = "apple_ukraine_golden"
            break;

          case 9:
            this.fruit = "apple"
            this.country="ukraine"
            this.active_element = "apple_ukraine_gala"
            break;

          case 10:
            this.fruit = "apple"
            this.country="poland"
            this.active_element = "apple_poland_golden"
            break;

          case 11:
            this.fruit = "apple"
            this.country="poland"
            this.active_element = "apple_poland_kalvin"
            break;

          default:
            this.fruit = null
            this.country=null
            this.active_element = null
            console.log('error')
            break;
        }
      },
    }

  }
</script>

<style scoped>

  .container {
    position: relative;
    display: block;
    width: 40%;
    text-align: center;
    margin: 0 auto;

  }

  /*oranges*/

  .oranges-menu {
    width: 100%;
    display: inline-flex;
  }

  .oranges-tub {
    height: 20px;
    width: 100px;
    border: 3px solid orange;
  }

  .spain {
    border: 3px solid orangered;
  }

  .spa-in {
    color: orangered;
  }

  .turkish {
    border: 3px solid darkorange;
  }

  .tur {
    color: darkorange;
  }

  .tunis {
    border: 3px solid mediumorchid;
  }

  .tun {
    color: mediumorchid;
  }



  /*apples*/

  .apples-menu {
    width: 100%;
    display: inline-flex;
  }

  .apples-tub {
    height: 20px;
    width: 100px;
    border: 3px solid green;
  }

  .ukraine {
    border: 3px solid blue;
  }

  .uah {
    color: blue;
  }

  .poland {
    border: 3px solid olivedrab;
  }

  .pl {
    color: olivedrab;
  }


  /*active tree*/

  .active_fruit {
    border: 3px solid darkgray;
  }

  .active_link {
    color: darkgray;
  }


  /*mixin*/

  .spain, .turkish, .tunis, .ukraine, .poland {
    height: 20px;
    width: 200px;
  }

  p {
    position: relative;
    margin-top: 10px;
    font-size: 10px;
  }


</style>
