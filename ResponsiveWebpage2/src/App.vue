<template>
  <div id="app">
    <div class='container-fluid remove-margin'>
      <Navbar/>
      <div class='row'>
        <Sidebar/>
        <ConversationColumn/>
        <meetup-column/>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar';
import Sidebar from './components/Sidebar';
import ConversationColumn from './components/ConversationColumn';
import MeetupColumn from './components/MeetupColumn';

export default {
  name: 'app',
  components: {
    Navbar,
    Sidebar,
    ConversationColumn,
    MeetupColumn
  },
}
</script>

<style>
@import url('../colors.css');
@import url('css/main.css');
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.remove-margin {
  margin: 0 !important;
  padding: 0 !important;
}
</style>
