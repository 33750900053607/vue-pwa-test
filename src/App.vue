<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>TEST</h1>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div id='timerText'>0:00:00</div>
    <form name="alarm_form">
        <p>アラーム: <select name ='option_hours'>
            
            <option value='7'>07</option>
            <option value='8'>08</option>
            <option value='9'>09</option>
            <option value='10'>10</option>
            <option value='11'>11</option>
            <option value='12'>12</option>
            <option value='13'>13</option>
            <option value='14'>14</option>
            <option value='15'>15</option>
            <option value='16'>16</option>
            <option value='17'>17</option>
            <option value='18'>18</option>
            <option value='19'>19</option>
            <option value='20'>20</option>
            <option value='21' selected>21</option>
            <option value='22'>22</option>
            <option value='23'>23</option>
            <option value='24'>24</option>
            <option value='25'>25</option>
            <option value='26'>26</option>
            <option value='27'>27</option>
            <option value='28'>28</option>
            <option value='29'>29</option>
            <option value='30'>30</option>
        </select>
        <select name ='option_minutes'>
            <option value='0'>00</option>
            <option value='5'>05</option>
            <option value='10'>10</option>
            <option value='15'>15</option>
            <option value='20'>20</option>
            <option value='25'>25</option>
            <option value='30'>30</option>
            <option value='35'>35</option>
            <option value='40'>40</option>
            <option value='45'>45</option>
            <option value='50'>50</option>
            <option value='55'>55</option>
        </select> <span class="btn" id="set_btn">設定</span></p></form>

        <div class="container">
            <p>アラーム設定時刻</p>
            <ul id="parent_list">
            </ul>
        </div>
  </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
#timerText {
            color: #00aaff;
            font-size: 148px;
            margin: 30px auto;
            text-shadow: 0 1px 0 rgba(255, 255, 255, 0.5);
        }

        p {
            font-size: 20px;
        }

        select {
            font-size: 18px;
            padding: 3px;
        }

        .btn{
            margin-left: 5px;
            display: inline-block;
            font-weight: bold;
            width: 60px;
            padding: 0.5px;
            border-radius: 5px;
            box-shadow: 0 2px 0 #CDC9C9;
            background: #EEE9E9;
            cursor: pointer;
        }

        .delete_btn {
            margin-left: 15px;
            font-weight: bold;
            width: 60px;
            padding: 3px;
            border-radius: 5px;
            background: #FF4500;
            box-shadow: 0 2px 0 red;
            cursor: pointer;
            color: #fff;
        }

        .container {
            text-align: left;
            padding: 15px;
            margin: 0 auto;
            background: #e0e0e0;
            width: 350px;
            height: 190px;
        }
        .container p {
            font-size: 16px;
            margin: 5px;

        }

        .container li{
            margin-bottom: 7px; 
        }
</style>
