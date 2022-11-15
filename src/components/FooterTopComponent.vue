
<script>
export default {
  name: 'FooterTopComponent',
  data(){
    return {
      dcComicsMenu: [
        {
          text: 'Characters',
          href: '#'
      },
        {
          text: 'Comics',
          href: '#'
      },
        {
          text: 'Movies',
          href: '#'
      },
        {
          text: 'TV',
          href: '#'
      },
        {
          text: 'Games',
          href: '#'
      },
        {
          text: 'Videos',
          href: '#'
      },
        {
          text: 'News',
          href: '#'
      },
    ],
      shopMenu: [
        {
          href: '#',
          text: 'Shop DC'
        },
        {
          href: '#',
          text: 'Shop DC Collectibles'
        }
      ],
      dcMenu: [
        {
          text: 'Terms Of Use',
          href: '#'
        },
        {
          text: 'Privacy policy (new)',
          href: '#'
        },
        {
          text: 'Ad Choices',
          href: '#'
        },
        {
          text: 'Advertising',
          href: '#'
        },
        {
          text: 'Jobs',
          href: '#'
        },
        {
          text: 'Subscriptions',
          href: '#'
        },
        {
          text: 'Talent Workshops',
          href: '#'
        },
        {
          text: 'CPSC Certicates',
          href: '#'
        },
        {
          text: 'Ratings',
          href: '#'
        },
        {
          text: 'Shop Help',
          href: '#'
        },
        {
          text: 'Contact Us',
          href: '#'
        },
      ],
      sitesMenu: [
        {
          text: 'DC',
          href: '#'
        },
        {
          text: 'MAD Magazine',
          href: '#'
        },
        {
          text: 'DC Kids',
          href: '#'
        },
        {
          text: 'DC Universe',
          href: '#'
        },
        {
          text: 'DC Power Visa',
          href: '#'
        },
      ]
    }
  }
}
</script>

<template>

  <footer>


    <div class="container">

      <div class="col">

        <div class="column-list">
          <h4>DC COMICS</h4>
          <ul>
            <li
            v-for="(item, index) in dcComicsMenu"
            :key="index"
            ><a :href="item.href">{{item.text}}</a></li>
          </ul>
        </div>

        <div class="column-list">
          <h4>SHOP</h4>
          <ul>
            <li
            v-for="(item, index) in shopMenu"
            :key="index"
            ><a :href="item.href">{{item.text}}</a></li>
          </ul>
        </div>

      </div>

      <div class="col">

        <div class="column-list">
          <h4>DC</h4>
          <ul>
            <li
            v-for="(item, index) in dcMenu"
            :key="index"
            ><a :href="item.href">{{item.text}}</a></li>
          </ul>
        </div>

      </div>

      <div class="col">

        <div class="column-list">
          <h4>SITES</h4>
          <ul>
            <li
            v-for="(item, index) in sitesMenu"
            :key="index"
            ><a :href="item.href">{{item.text}}</a></li>
          </ul>
        </div>

      </div>
      
    </div>


    <img src="../../vue-dc-comics-1/img/dc-logo-bg.png" alt="Logo DC">
  </footer>


</template>

<style lang="scss" scoped>

@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

h4 {
  color: white;
  font-size: $bigger-font-size;
  margin-bottom: 10px;
}

.container {
  display: flex;
}

footer {
  height: 600px;
  background-image: url(../../vue-dc-comics-1/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  overflow: hidden;
  padding-top: 55px;
  img {
    position: absolute;
    top: -25px;
    right: 255px;
    transform: scale(1.4);
  }
}

.col {
  padding: 0 15px;
  li {
    padding: 7px 0;
    a {
      color: rgb(153, 153, 153);
      &:hover {
        color: white;
      }
    }

  }
  .column-list:nth-child(2){
    margin-top: 30px;
  }
}

</style>