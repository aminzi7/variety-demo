<template>
  <div id="app" class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="swiper-container">
          <div class="timeline">
            <div class="swiper-slide" v-for="(item, index) in dataV" :key="index">
              <div class="timestamp">
                <span class="date"> {{ item.dateLabel }} </span>
              </div>
              <div class="status">
                <span>{{ item.title }}</span>
              </div>
            </div>
          </div>
          <!-- Add Pagination -->
          <div class="swiper-pagination">
            <div class="timeline">
              <div class="swiper-slide" v-for="(item, index) in dataV" :key="index">
                <div class="timestamp">
                  <span class="date"> {{ item.dateLabel }} </span>
                </div>
                <div class="status">
                  <span>{{ item.title }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const dataV = [
  { dateLabel: 'January 2017', title: 'Gathering Information' },
  { dateLabel: 'February 2017', title: 'Planning' },
  { dateLabel: 'March 2017', title: 'Design' },
  { dateLabel: 'April 2017', title: 'Content Writing and Assembly' },
  { dateLabel: 'May 2017', title: 'Coding' },
  { dateLabel: 'June 2017', title: 'Testing, Review & Launch' },
  { dateLabel: 'July 2017', title: 'Maintenance' }
]
</script>

<style scoped>
.timeline {
  margin: 50px 0;
  list-style-type: none;
  display: flex;
  padding: 0;
  text-align: center;
}
/* .timeline li {
  transition: all 200ms ease-in;
} */
.timestamp {
  width: 200px;
  margin-bottom: 20px;
  padding: 0px 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-weight: 100;
}
.status {
  padding: 0px 40px;
  display: flex;
  justify-content: center;
  border-top: 4px solid #3e70ff;
  position: relative;
  transition: all 200ms ease-in;
}

.status span {
  font-weight: 600;
  padding-top: 20px;
}
.status span:before {
  content: '';
  width: 25px;
  height: 25px;
  background-color: #e8eeff;
  border-radius: 25px;
  /* border: 4px solid #3e70ff; */
  border: 4px solid #77ff00;
  position: absolute;
  top: -15px;
  left: 42%;
  transition: all 200ms ease-in;
}
.swiper-control {
  text-align: right;
}

.swiper-container {
  width: 100%;
  height: 250px;
  margin: 50px 0;
  overflow: hidden;
  padding: 0 20px 30px 20px;
}
.swiper-slide {
  width: 200px;
  text-align: center;
  font-size: 18px;
}
.swiper-slide:nth-child(2n) {
  width: 40%;
}
.swiper-slide:nth-child(3n) {
  width: 20%;
}
</style>
