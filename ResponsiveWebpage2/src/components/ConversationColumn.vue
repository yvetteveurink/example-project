<template>
  <div class='col-12 col-sm column-wrapper rounded-left'>
    <div class='container'>
      <div class='row'>
        <h1 class='title col-11 mx-auto text-light mt-3 py-2'>Conversations</h1>
      </div>
      <div class='inner-container col-11 mx-auto bg-light text-black rounded' v-for='item in json' v-bind:key='item._id' v-if='item.type === "conversation"'>
        <div class='row'>
          <div class='col-3'>
            <img class='img-fluid rounded-circle float-left size-avatar ml-3 mt-3' src='../assets/female_avatar.jpg'>
          </div>
          <div class='col-9'>
            <h1></h1><br /><h5 class='text-left ml-2 mt-4'>{{item.author.name}} <br /><small>{{item.author.profession}}, {{item.title}}</small></h5>
          </div>
        </div>
        <div class='speech-bubble mt-4 w-75 mx-auto text-light'>
          <h6 class='py-2 medium-text'>{{item.body}}</h6>
        </div>
        <div class='row mt-3 smallest-text'>
          <div class='col'>22 September 2017</div>
          <div class='col'><i class="far fa-gem fa-lg px-1"></i>{{item.likes}} waarderingen</div>
          <div class='col'>
            <i class='fas fa-comments fa-lg px-1'></i>{{item.comments.length}} reacties
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ListData from '../../listdata.json';

export default {
  name: 'conversationColumn',
  data(){
    return{
      json: ListData
    }
  }
}
</script>


<style>
  .title {
    font-size: 2em;
    background-color: var(--secondary-bg-color);
    border-radius: 5px;
    box-shadow: 5px 5px 20px var(--shadow);
  }

  .size-avatar {
    min-height: 50px;
    min-width: 50px;
  }

  .speech-bubble {
    position: relative;
    background: var(--secondary-bg-color);
	  border-radius: .4em;
}

.speech-bubble:after {
	content: '';
	position: absolute;
	top: 0;
	left: 50%;
	width: 0;
	height: 0;
	border: 0.875em solid transparent;
	border-bottom-color: var(--secondary-bg-color);
	border-top: 0;
	margin-left: -0.875em;
	margin-top: -0.875em;
}
</style>





