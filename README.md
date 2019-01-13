
<input type="text" name="spanishPhrase">

<button onclick="speakSpanish()">Click here to hear spanish.</button>
 
<script>
 
function speakSpanish() { 
   //var val= prompt("Enter Spanish phrase",""); 
   var val = $('#spanishPhrase').val();
    if (val) 
        location="https://audio1.spanishdict.com/audio?detect_lang=true&text="+val.replace(/\s+/g, '-').toLowerCase()+"&format=mp3";
}
</script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
