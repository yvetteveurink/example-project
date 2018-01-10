<template>
  <div class='col-12 col-sm column-wrapper'>
    <div class='container'>
      <div class='row'>
        <h1 class='title col-11 mx-auto text-light mt-3 py-2'>Planned meetups</h1>
      </div>
      <div class='inner-container bg-cover col-11 mx-auto rounded pt-5' v-for='item in json' v-bind:key='item._id' v-if='item.type === "meetup"' v-bind:style="{ backgroundImage: 'url(' + item.background + ')' }">
        <div class='col-8 ml-3 mt-5 mb-3 bg-grey text-light'>
          <div class='row'>
            <p class='col-3 mt-3 text-left medium-text'><strong>Meetup</strong></p>
            <p class='col-7 col-sm-9 col-md-7 col-lg-9 col-xl-7 mt-3 text-right medium-text'><i class="fas fa-thumbtack mr-1"></i><strong> {{item.location}}</strong></p>
          </div>
          <div class='col-10 col-sm-12 col-md-10 col-lg-12 col-xl-10 stripe bg-light'></div>
          <div class='row'>
            <div class='col-12 small-text text-left mt-3'>
              <i class="far fa-calendar-alt"></i> 22 September 2017 / 17:00 uur
            </div>
          </div>
          <div class='row'>
            <h4 class='col-10 text-left mt-2 large-text'>{{item.title}}</h4>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import listdata from '../../listdata.json';

export default {
  name: 'conversationColumn',
  data(){
    return{
      json: listdata,
    }
  }
}
</script>


<style>
  .bg-cover {
    background-size: cover;
  }

  .bg-grey {
    background-color: var(--secondary-bg-color);
  }
</style>
