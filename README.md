# Celpip
<h1>Prepare for Celpip Test</h1>
<h2>Count Words</h2>
<pre><code>
<script>

function changeCount() {
  var val = document.getElementById("userTxt").value;
  var count = countWords(val);

  document.getElementById("count").innerText = count;
}

function countWords(s){
  s = s.replace(/(^\s*)|(\s*$)/gi,"");//exclude  start and end white-space
  s = s.replace(/[ ]{2,}/gi," ");//2 or more space to 1
  s = s.replace(/\n/g, ' '); //Enter Key -> replace Space
  return s.split(' ').filter(function(str){return str!="";}).length;
}
</script>
  <textarea style="width:100%; height:auto;" 
  onclick="this.select()" onfocus="this.select()" 
  id="userTxt" rows="20" cols="60"  
  onkeyup="changeCount();">
  </textarea>
  <br/>
  <span id="count">0</span>
</code></pre>

