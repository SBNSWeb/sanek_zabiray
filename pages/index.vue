<template>
<div>
  
  <v-container>
    <v-carousel v-model="model">
    <v-carousel-item
      v-for="(color, i) in colors"
      :key="color"
    >
      <v-sheet
        :color="color"
        height="100%"
        width="100%"
        tile
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"

        >
          <div class="display-3">
            <img src="https://u-stena.ru/upload/iblock/526/5269612cdf011df68e0cbcd639ba0129.jpg" alt="">
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
  <h1>Main Division</h1>
  <v-simple-table class="mt-3">
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Command
          </th>
          <th class="text-left">
            Score
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
          <td>{{ item.name }}</td>
          <td>{{ item.calories }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>

  <v-divider></v-divider>
  <h1>About Our League</h1>
<v-alert
      class="mt-4"
      color=""
      dark
      icon="mdi-vuetify"
      border="left"
      prominent
    >
      The Football League consists of 69 professional association football clubs in England and 3 in Wales. It runs the oldest professional football league competition in the world. It also organizes two knockout cup competitions, the EFL Cup and EFL Trophy. The Football League was founded in 1888 by then-Aston Villa director William McGregor, originally with 12 member clubs. Steady growth and the addition of more divisions meant that by 1950 the League had 92 clubs. Financial considerations led to a major shake-up in 1992, when in a step to maximize their revenue the leading members of the Football League broke away to form their own competition, the FA Premier League, which was renamed the Premier League in 2007. The Football League therefore no longer includes the top 20 clubs who belong to this group, although promotion and relegation between the Football League and the Premier League continues. In total, 136 teams have played in the Football League up to 2013 (including those in the Premier League, since clubs must pass through the Football League before reaching the former).
    </v-alert>

  </v-container>
</div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  //json cюда
  data: () =>  ({
      model: 0,

      //colors: [
      //    {
      //      src: 'https://mediasat.info/wp-content/uploads/2019/07/Goal-Soccer.jpg',
      //    },
      //    {
      //      src: 'https://mediasat.info/wp-content/uploads/2019/07/Goal-Soccer.jpg',
      //    },
      //    {
      //      src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
      //    },
      //    {
      //      src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
      //    },
      //],

      colors:[
        '<img src="https://i.ytimg.com/vi/YDPWXnBudA0/maxresdefault.jpg" alt="">',
        'green',
        'yellow darken-2',
        'red',
        'orange',
      ],

        desserts: [
          {
            name: 'Jupiter',
            calories: 228,
          },
          {
            name: 'Black pearl',
            calories: 227,
          },
          {
            name: 'Haliky',
            calories: 211,
          },
          {
            name: 'Gaik',
            calories: 200,
          },
          {
            name: '13shka',
            calories: 199,
          },
          {
            name: 'Telegi',
            calories: 180,
          }
        ],
        show: false,
    }),
}
</script>
