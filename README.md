<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title></title>
  <style>
    #container{
      background-color: floralwhite;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      
    }
    
    #calculator{
      background-color: gray;
      padding:20px;
      margin-top: 10px;
      border-radius: 10px;
      width: 300px;
      box-shadow: 7px 7px 5px black ;
      
      
    }
    input{
      height: 60px;
      width: 60px;
      background-color: lightblue;
      color: #fff;
      border-radius: 10px;
      box-shadow: 3px 3px 1px lightcyan ;
       
      margin: 5px;
      font-size: 30px;
      font: bold;
    }
    
    #screen_area{
      width: 280px;
      background-color: skyblue;
      text-align: right;
      color: deeppink;
      box-shadow: none;
      
    }
    
    .screen{
      padding-bottom: 20px;
    }
    
    #input_equal{
      width: 135px;
      background-color: violet;
      color: aqua;
    }
    
    .operator_button{
      color: violet;
    }
    
    span{
      display: flex;
      text-align: end;
      justify-content: center;
      font-size: 15px;
      color: white;
      font: bold;
    }
    
     #logo{
      display: grid;
      justify-content: center;
      padding-bottom: 10px;
      
      
      
    }

  </style>
</head>

<body>
  
  <div id="container">
    <div id="calculator">
      <form>
        
        <div id="logo"><img src="https://i.postimg.cc/zfbYqj3b/Picsart-23-03-27-22-09-10-193.png" height="40" width="40"></div>
        
        <div class="screen">
          <input type="text" contenteditable="false" name="display" id="screen_area">
        </div>
        
        <div>
          
          <input type="button" value="AC" class="operator_button" onclick="press_AC()">
          
          <input type="button" value="C" class="operator_button"  onclick="press_C()">
          
          <input type="button" value="." class="operator_button" onclick="press_dot()">
          
          <input type="button" value="/" class="operator_button" onclick="press_divide()">
          
        </div>
        <div>
          
          <input type="button" value="1" onclick="press_1()">
          <input type="button" value="2" onclick="press_2()">
          <input type="button" value="3" onclick="press_3()">
          <input type="button" value="*" onclick="press_multiply()" class="operator_button">
          
        </div>
        <div>
          
          <input type="button" value="4" onclick="press_4()">
          <input type="button" value="5" onclick="press_5()">
          <input type="button" value="6" onclick="press_6()">
          <input type="button" value="-" onclick="press_sub()" class="operator_button">
          
        </div>
        <div>
          
          <input type="button" value="7" onclick="press_7()">
          <input type="button" value="8" onclick="press_8()">
          <input type="button" value="9" onclick="press_9()">
          <input type="button" value="+" onclick="press_add()" class="operator_button">
        </div>
        <div>
          <input type="button" value="00" onclick="press_00()">
          <input type="button" value="0" onclick="press_0()">
          <input type="button" value="=" onclick="press_equal()" class="operator_button" id="input_equal">
          
        </div>
        <span><p>Abhishek calculator</p></span>

      </form>
    </div>
    
  </div>
  
  <script>



  
  const press_1 = () =>   document.getElementById("screen_area").value  += "1"
  
  const press_2 = () =>   document.getElementById("screen_area").value  += "2"
  
  const press_3 = () =>   document.getElementById("screen_area").value  += "3"
  
  const press_4 = () =>   document.getElementById("screen_area").value  += "4"
  
  const press_5 = () =>   document.getElementById("screen_area").value  += "5"
  
  const press_6 = () =>   document.getElementById("screen_area").value  += "6"
  
  const press_7 = () =>   document.getElementById("screen_area").value  += "7"
  
  const press_8 = () =>   document.getElementById("screen_area").value  += "8"
  
  const press_9 = () =>   document.getElementById("screen_area").value  += "9"
  
  const press_00 = () =>   document.getElementById("screen_area").value  += "00"
  
  const press_0 = () =>   document.getElementById("screen_area").value  += "0"
  
  const press_dot = () =>   document.getElementById("screen_area").value  += "."
  
  const press_add = () =>   document.getElementById("screen_area").value  += "+"
  
  const press_sub = () =>   document.getElementById("screen_area").value  += "-"
  
  const press_multiply = () =>   document.getElementById("screen_area").value  += "*"
  
  const press_divide = () =>   document.getElementById("screen_area").value  += "/" 
  
  const press_AC = () =>   document.getElementById("screen_area").value  = " "
  
  
    
  const press_C = () => {
    
    const user_input = document.getElementById("screen_area").value ;
    
    const delete_ele = user_input.toString().slice(0 , -1);
    
    document.getElementById("screen_area").value = `${delete_ele}`
  
  }
  
  
  const press_equal = () => {
    
  const user_input = document.getElementById("screen_area").value ;
  
  const Calculation =  eval(user_input);
  
  document.getElementById("screen_area").value = `${Calculation}`
  
const Textarea_element_value = document.getElementById("screen_area").value
  
  
  const text_to_speech = new SpeechSynthesisUtterance(Textarea_element_value)
  
  
  
  speechSynthesis.speak(text_to_speech)
  
  
  
  }
  
  
  </script>
  
  
  
</body>



</html>
