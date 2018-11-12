# Celpip
<h1>Prepare for Celpip Test</h1>
<h2>Speaking</h2>


![Speaking Test Form](https://github.com/kwakchulyong/Celpip/blob/master/screenshot/speakingtestform.png)

<h2>Count Words</h2>
<pre><code>
<body>
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
	
	function download() {
		var resultText = document.getElementById("userTxt").value;
		var hiddenElement = document.createElement('a');

		//hiddenElement.href = 'data:attachment/text,' + encodeURI(resultText);
		hiddenElement.href = 'data:attachment/text,' + encodeURIComponent(resultText);
		hiddenElement.target = '_blank';
		hiddenElement.download = 'testEssay.txt';
		hiddenElement.click();
		
		alert('Complete Download');
	}
	
	</script>
  
  
  <textarea style="width:100%; height:auto;" 
  onfocus="this.select()" 
  id="userTxt" rows="20" cols="60"  
  onkeyup="changeCount();">
  </textarea>
  <br/>
  <span id="count">0</span> <button onclick="download();">download</button>
</body>
</code></pre>

