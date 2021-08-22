<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title></title>
</head>

<body>
  
 <style type="text/css" media="all">
   *{
     margin: 0;
     padding: 0;
     box-sizing: border-box
   }
   body{
     width: 100%;
     height: 100%;
     background: black;
   }
  .main{
    width: 100%;
    height: 100%;
    border: 3px double white;
    border-radius: 6px;
    display: flex;
    flex-direction: column;
  }
.box{
  width: 90%;
  height: 50vh;
  border: 0px solid white;
  border-radius: 5px;
  margin:50px auto;
  box-shadow:-1px 1px 9px 3px white;
transition:1s;
position: relative;
  
}
.box:hover{
  
 box-shadow:-1px 1px 9px 1px yellow;
}

.box2{
  width: 80%;
  height: 80%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform-style: preserve-3d;
  transform: translate(-50%,-50%) rotate(-90deg);
}


.box .main-network{
  
  
  border: 2px solid white;
  width: calc(var(--i)*16%);
  height: 40px;
  border-radius: 50px;
  margin: 10px 0px;
  position: relative;
 overflow: hidden;
  
}
.main-network::before{
  content: "";
  background: linear-gradient(blue,blue);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
  border-radius: 30px;
  animation: network 10s linear infinite;
  animation-delay: calc(var(--i)*0.5s);
/*  transform: rotatey(90deg);*/
  background-size:  0% auto;
  background-repeat: no-repeat;
  
}

@keyframes network{
  0%,100%{ 
    
    background-size:  0% auto;
 
  }
40%, 50%,60%{
 /*   transform-origin: left;*/
/*transform: translateX(0%)*/
background-size:  100% auto;
  }
}




 </style>
  
<div class="main">
  
  
  
  <div class="box">
    <div class="box2">
    <div class="main-network"style="--i:1"></div>
    <div class="main-network"style="--i:2"></div>
    <div class="main-network"style="--i:3"></div>
    <div class="main-network"style="--i:4"></div>
    <div class="main-network"style="--i:5"></div>
    </div>
  </div>
  
  
  <div class="box"></div>
  
  
  <div class="box"></div>
  
  
  <div class="box"></div>
  
  
</div>
</body>

</html>
