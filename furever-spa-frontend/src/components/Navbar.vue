<template>
  <div id="navbar">
    <ul style='background-color: rgb(255, 253, 232);'>
          <li style="cursor: pointer;" onclick="$('.navTrigger').toggleClass('active');">
            <a>
              <div class="navTrigger">
                <i></i><i></i><i></i>
              </div>
            </a>
          </li>   
        <li style="display:inline-block"><img src="../assets/logo.png" height="40px" style="margin-top:10px; position: absolute; right: 47vw"><li>
        <li class="cogs" style="float:right" onmouseover="function() { $('#cog1').removeClass('paused'); $('#cog1').addClass() }" onmouseout="function() { $('#cog1').addClass('paused'); }">
          <a to="settings" class="nav-item" exact>
            <div class="three-cogs fa-1x">
              <i class="fa fa-cog fa-2x fa-fw spin" id="cog1"></i>
              <i class="fa fa-cog fa-1x fa-fw spin-back" id="cog2"></i>
            </div>
          </a>
        </li>

        <li style="float:right">
          <a to="login" class="nav-item" exact>
            <i class="fas fa-user" style="margin-top: 10px"></i>
          </a>
        </li>

        <li style="float:right">
          <a to="saved" class="nav-item" exact>
            <i class="fas fa-heart" style="margin-top: 10px"></i>
          </a>
        </li>
    </ul> 
  </div>

</template>

<script>
  export default {
    name: 'navbar',
  }
</script>

<style>

.cogs:hover .spin, .cogs:hover .spin-back {
  animation-play-state: running;
}

.three-cogs {
	 position: relative;
   padding-top: 5px;
}

.spin {
  animation: cog-spin 4s infinite linear;
  animation-play-state: paused;
}

#cog2 {
  position: absolute;
  top: -0.05em;
  right: -0.25em;
}

.spin-back {
  animation: cog-spin 2s infinite linear;
  animation-direction: reverse;
  animation-play-state: paused;
}

@keyframes cog-spin {
  from {
        transform:rotate(0deg);
    }
  to {
    transform:rotate(360deg);
  }
}
 

#navbar {
    position: fixed;
    width: 100%;
    z-index: 100;
}

.navMenu {
  cursor: pointer;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  height: 68px;
  width: 72px;
}

/* Change the link color on hover */
li a:hover {
  background-color: rgb(182, 182, 182);
}


/* Code from https://codepen.io/dicson/pen/waKPgQ used under education license */

.navTrigger {
	 cursor: pointer;
	 width: 30px;
	 height: 25px;
	 margin: auto;
   margin-top: 8px;
}
 .navTrigger i {
	 background-color: #000;
	 border-radius: 2px;
	 content: '';
	 display: block;
	 width: 100%;
	 height: 4px;
}
 .navTrigger i:nth-child(1) {
	 -webkit-animation: outT 0.8s backwards;
	 animation: outT 0.8s backwards;
	 -webkit-animation-direction: reverse;
	 animation-direction: reverse;
}
 .navTrigger i:nth-child(2) {
	 margin: 5px 0;
	 -webkit-animation: outM 0.8s backwards;
	 animation: outM 0.8s backwards;
	 -webkit-animation-direction: reverse;
	 animation-direction: reverse;
}
 .navTrigger i:nth-child(3) {
	 -webkit-animation: outBtm 0.8s backwards;
	 animation: outBtm 0.8s backwards;
	 -webkit-animation-direction: reverse;
	 animation-direction: reverse;
}
 .navTrigger.active i:nth-child(1) {
	 -webkit-animation: inT 0.8s forwards;
	 animation: inT 0.8s forwards;
}
 .navTrigger.active i:nth-child(2) {
	 -webkit-animation: inM 0.8s forwards;
	 animation: inM 0.8s forwards;
}
 .navTrigger.active i:nth-child(3) {
	 -webkit-animation: inBtm 0.8s forwards;
	 animation: inBtm 0.8s forwards;
}
 @-webkit-keyframes inM {
	 50% {
		 -webkit-transform: rotate(0deg);
	}
	 100% {
		 -webkit-transform: rotate(45deg);
	}
}
 @keyframes inM {
	 50% {
		 transform: rotate(0deg);
	}
	 100% {
		 transform: rotate(45deg);
	}
}
 @-webkit-keyframes outM {
	 50% {
		 -webkit-transform: rotate(0deg);
	}
	 100% {
		 -webkit-transform: rotate(45deg);
	}
}
 @keyframes outM {
	 50% {
		 transform: rotate(0deg);
	}
	 100% {
		 transform: rotate(45deg);
	}
}
 @-webkit-keyframes inT {
	 0% {
		 -webkit-transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 -webkit-transform: translateY(9px) rotate(0deg);
	}
	 100% {
		 -webkit-transform: translateY(9px) rotate(135deg);
	}
}
 @keyframes inT {
	 0% {
		 transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 transform: translateY(9px) rotate(0deg);
	}
	 100% {
		 transform: translateY(9px) rotate(135deg);
	}
}
 @-webkit-keyframes outT {
	 0% {
		 -webkit-transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 -webkit-transform: translateY(9px) rotate(0deg);
	}
	 100% {
		 -webkit-transform: translateY(9px) rotate(135deg);
	}
}
 @keyframes outT {
	 0% {
		 transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 transform: translateY(9px) rotate(0deg);
	}
	 100% {
		 transform: translateY(9px) rotate(135deg);
	}
}
 @-webkit-keyframes inBtm {
	 0% {
		 -webkit-transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 -webkit-transform: translateY(-9px) rotate(0deg);
	}
	 100% {
		 -webkit-transform: translateY(-9px) rotate(135deg);
	}
}
 @keyframes inBtm {
	 0% {
		 transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 transform: translateY(-9px) rotate(0deg);
	}
	 100% {
		 transform: translateY(-9px) rotate(135deg);
	}
}
 @-webkit-keyframes outBtm {
	 0% {
		 -webkit-transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 -webkit-transform: translateY(-9px) rotate(0deg);
	}
	 100% {
		 -webkit-transform: translateY(-9px) rotate(135deg);
	}
}
 @keyframes outBtm {
	 0% {
		 transform: translateY(0px) rotate(0deg);
	}
	 50% {
		 transform: translateY(-9px) rotate(0deg);
	}
	 100% {
		 transform: translateY(-9px) rotate(135deg);
	}
}
 
</style>