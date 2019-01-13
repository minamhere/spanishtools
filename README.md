<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

<input type="text" id="spanishPhrase"> <button onclick="speakSpanish()">Click here to hear spanish.</button>
 
<script>
 
function speakSpanish() { 
   var val = $('#spanishPhrase').val();
   if (val) 
        location="https://audio1.spanishdict.com/audio?detect_lang=true&text="+val.replace(/\s+/g, '-').toLowerCase()+"&format=mp3";
}

$('#spanishPhrase').on('keypress', function (e) {
         if(e.which === 13){

            //Disable textbox to prevent multiple submit
            $(this).attr("disabled", "disabled");

            //Do Stuff, submit, etc..
            speakSpanish();

            //Enable the textbox again if needed.
            $(this).removeAttr("disabled");
         }
   });
   
</script>

