<!doctype html>
<html>
<head>
	<meta charset="utf-8">
	<title>test page</title>
</head>
<!doctype html>
<html>
<head>
	<meta charset="utf-8">
	<title>test page</title>
	<style>
		body{
  margin: 0;
  padding: 0;
  font-family: "Montserrat";
}
.searchbox{
  width: 90%;
  margin: 10px auto;
}
.header{
  background: #ECDFBF;
  overflow: hidden;
  padding: 20px;
  text-align: center;
}
.header h1{
  text-transform: uppercase;
  color: white;
  margin: 0;
  margin-bottom: 8px;
}
#value{
  border: none;
  background: #E0D3B6;
  padding: 6px;
  font-size: 18px;
  width: 80%;
  border-radius: 6px;
  color: white;
}
#value:focus{
  outline: none;
}
.container{
  background: #FFFFF5;
  padding: 1%;
}
.item{
  margin: 3% 0px;
  display: flex;
  align-items: center;
}
.icon{
  width: 25px;
  height: 25px;
  background: #E0D3B6;
  color: white;
  font-size: 15px;
  text-align: center;
  line-height: 25px;
  border-radius: 50%;
  margin-right: 8px;
}
.name{
  font-size: 17px;
  font-weight: 470;
  color: #333;
}
	</style>
	
</head>
<body>
   <div class="searchbox">
      <div class="header">
        <h1>Search</h1>
        <input onkeyup="filter()" type="text" id="value" placeholder="Type to Search">
      </div>

      <div class="container">

        <div class="item">
          <span class="icon">A</span>
          <span class="name">Apple</span>
        </div>

        <div class="item">
          <span class="icon">O</span>
          <span class="name">Orange</span>
        </div>

        <div class="item">
          <span class="icon">M</span>
          <span class="name">Mandarin</span>
        </div>

        <div class="item">
          <span class="icon">S</span>
          <span class="name">Strawberry</span>
        </div>

        <div class="item">
          <span class="icon">W</span>
          <span class="name">Watermelon</span>
        </div>

      </div>
    </div>
<script type="text/javascript">
      function filter(){

        var value, name, item, i;

        value = document.getElementById("value").value.toUpperCase();
        item = document.getElementsByClassName("item");

        for(i=0;i<item.length;i++){
          name = item[i].getElementsByClassName("name");
          if(name[0].innerHTML.toUpperCase().indexOf(value) > -1){
            item[i].style.display = "flex";
          }else{
            item[i].style.display = "none";
          }
        }
      }
</script>
</body>

</html>
</html>
