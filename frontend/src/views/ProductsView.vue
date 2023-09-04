<template>
  <div class="Landing">
<h3 class="comp">GOLDEN RIMZ CUSTOMZ</h3>
<h1 class="show">SHOWROOM</h1>
<div class="quality">
  <p><img src="../assets/check-solid.svg" alt="" style="height: 30px; color: white;"> &nbsp;<b>Best quality custom vehicles</b></p>
</div>
<div class="check">
  <p><img src="../assets/check-solid.svg" alt="" style="height: 30px; color: white;">&nbsp;<b>Quality assured products</b></p>
</div>

  </div> 
  <br>
  <div class="Showroom">
<div class="Brands">
<h4>Brands</h4>
<hr>
<p>AUDI</p>
<p>BMW</p>
<p>MERCEDES</p>
<p>VW</p>
<p>LAND ROVER</p>
<p>TOYOTA</p>

<hr>
<p>SHOW ALL BRANDS</p>

</div>
<div class="Transmition">
  <h4>Transmition</h4>
  <select id="Transmit">
  <option value="Manual">Manual</option>
  <option value="Automatic">Automatic</option>
</select>
  

</div>
<div class="Fuel">
  <h4>Fuel Type</h4>
  <select id="Transmit">
  <option value="Manual">Diesel</option>
  <option value="Automatic">Petrol</option>
  <option value="Manual">Hybrid</option>
  <option value="Automatic">Electric</option>
</select>
  

</div>


  </div> 
  <br>
</template>
<style scoped>
.Landing{
    background-image: url(https://i.postimg.cc/9FvxFHgr/3ff5188ff22ded5d23bd9f85f06ed656.gif);
    height: 60vh;
    background-repeat: no-repeat;
    background-position-x: right;
    background-size:contain;
    background-color: #333333;
    text-align: left;
    box-shadow: 2px 3px 3px white;
  

}
.comp{
padding-left: 10%;
padding-top: 10%;
font-family: 'Black Ops One', cursive;
  color: gold;
}
.show{
  padding-left: 10%;
  color: maroon;
  font-family: 'Black Ops One', cursive;
}
.quality{
 background-color: white;
 height: 30px;
 width: 300px;
 margin-inline-start: 100px;
 border-radius: 30px;
 color: maroon;
 padding-left: 8px;
 
}
.check{
 background-color: white;
 height: 30px;
 width: 300px;
 margin-inline-start: 100px;
 border-radius: 30px;
 color: maroon;
 padding-left: 8px;
 margin-top: 15px;
 
}
.Showroom{
height: 100vh;
background-color: black;

}
.Brands{
height: 350px;
width: 200px;
background-color:azure;
margin-left: 50px;
border-radius: 5%;
}
.Transmition{
  margin: 20px;
height: 80px;
width: 200px;
background-color:azure;
margin-left: 50px;
margin-bottom: -10px;
border-radius: 5%;
}
.Fuel{
  margin: 20px;
height: 80px;
width: 200px;
background-color:azure;
margin-left: 50px;
margin-bottom: -10px;
border-radius: 5%;
}


h4{
  color: maroon;
}

</style>