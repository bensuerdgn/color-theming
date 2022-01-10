<template>
  <div class="section">
    <div class="section-container">
      <div class="section-container-top">
        <div class="cloud">
          <h1>WELCOME TO WEBSITE</h1>
          <div class="build"></div>
        </div>
      </div>
      <div class="section-container-bottom">
        <div class="section-container-bottom-first">
          <div class="section-container-title"><p>FEATURE</p></div>
          <div class="section-container-text">
            <h1>All You Need To Grow Online.</h1>
          </div>
          <div class="section-container-items">
            <div class="item" v-for="item in items" :key="item">
              <div class="item-img">
                <img :src="require(`@/assets/images/${item.img}`)" alt="" />
              </div>
              <div class="item-title">
                <h3>{{ item.title }}</h3>
              </div>
              <div class="item-text">
                <p>
                  {{ item.text }}
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="section-container-bottom-second">
          <div
            class="second-item"
            :class="'second-item-'+item.id"
            v-for="item in items2"
            :key="item"
          >
            <div class="text">
              <p>{{ item.title }}</p>
              <h1>{{ item.title2 }}</h1>
              <h3>{{ item.text }}</h3>
              <div class="button">
                <button>LEARN MORE</button>
              </div>
            </div>
            <div class="image">
              <img :src="require(`@/assets/images/${item.image}`)" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          img: "cloud.svg",
          title: "Easy to customize",
          text: "Perfect domain name allows you to present your brand in the best light.",
        },
        {
          img: "settings.svg",
          title: "Build It",
          text: "Our powerful, reliable web hosting backs your site on a stable & secure platform.",
        },
        {
          img: "support.svg",
          title: "24/7 Supports",
          text: "24/7/365 Premium Support via Phone, Live Chat and Online Support Portal.",
        },
      ],
      items2: [
        {
          id: "1",
          title: "EASY INTEGRATIONS",
          title2: "Fast, Secure And Always Online.",
          text: "With industry-leading load times, guaranteed 99.9% uptime and expert, 24/7 support, your site couldn’t ask for more.",
          image: "illustration1.png",
        },
        {
          id: "2",
          title: "SMART DEPLOYMENT",
          title2: "Deploy And Scale Seamlessly",
          text: "Deploy to any of our data center locations – New York, SF, London, Amsterdam, Bangalore, and more.",
          image: "illustration2.png",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>