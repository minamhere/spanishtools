
<input type="text" name="spanishPhrase"></input>

<button onclick="speakSpanish(spanishPhrase.value)">Click here to hear spanish.</button>
 
<script>
function speakSpanish(val) { 
   //var val= prompt("Enter Spanish phrase",""); 
    if (val) 
        location="https://audio1.spanishdict.com/audio?detect_lang=true&text="+val.replace(/\s+/g, '-').toLowerCase()+"&format=mp3";
}
</script>
