<div align="center">

## Trivia Quiz


</div>

### Description

This is a cool javascript that creates a Trivia Quiz. You can change the number of questions, answers, and time allowed to answer the question. When all questions are done, it displays the amount of questions correct.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[darocker22](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/darocker22.md)
**Level**          |Intermediate
**User Rating**    |4.9 (39 globes from 8 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/darocker22-trivia-quiz__2-2619/archive/master.zip)





### Source Code

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<html>
<head>
<style type="text/css">
a,a:active, a:visited {color:blue; text-decoration:none;}
a:hover {color:red; text-decoration:none;}
</style>
<script language="javascript">
// how many seconds available to answer each question
var delay=15;
// an array listing the correct answer for each question in order of appearance
var correctAnswers=new Array("c","c","d","a","c","c","a","c","c","b");
// =====================================================
// do not change script below this line
// =====================================================
var q_num=1;
var timer;
var layer;
var clock=delay;
var score=0;
function show_question(){
	if (layer=eval("document.all.question"+q_num)){
		layer.style.display="inline";
		document.all.timeLeft.innerHTML=clock;
		hide_question();
	} else {
		document.all.timeLeft.innerHTML=0;
		document.all.quizScore.innerHTML="You have answered correctly "+score+" out of "+(q_num-1)+" questions.";
		document.all.quizScore.style.display="inline";
	}
}
function hide_question(){
	if (clock>0) {
		document.all.timeLeft.innerHTML=clock;
		clock--;
		timer=setTimeout("hide_question()",1000);
	} else {
		clearTimeout(timer);
		document.all.answerBoard.innerHTML="&nbsp;";
		clock=delay;
		layer.style.display="none";
		q_num++;
		show_question();
	}
}
function check_answer(answer){
	if (correctAnswers[q_num-1]==answer){
		score++;
		document.all.answerBoard.innerHTML="<i><b>Correct!</b></i>";
	} else {
		//clock=0
		hide_question();
		document.all.answerBoard.innerHTML="<i><b>Wrong!</b></i>";
	}
	clock=0;
	clearTimeout(timer);
	timer=setTimeout("hide_question()",1500);
}
window.onload=show_question;
</script>
</head>
<body>
Time left: <span id="timeLeft"></span>&nbsp; seconds<br>
<br>
<div id="answerBoard">&nbsp;</div>
<br>
<div id="question1" style="display:none">
<b>1. Who has NEVER played as a New York Knick?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) PATRICK EWING</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) TRAVIS KNIGHT</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) BRENT BARRY</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) JOHN STARKS</a><br>
</div>
<div id="question2" style="display:none">
<b>2. What player holds the record for most points scored at the NBA All-star rookie game with 31 points?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) MICHAEL JORDAN</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) ALLEN IVERSON</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) KOBE BRYANT</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) KEVIN GARNETT</a><br>
</div>
<div id="question3" style="display:none">
<b>3. When did the Sonics win their first championship?/b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) 1980</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) 1972</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) 1978</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) 1979</a><br>
</div>
<div id="question4" style="display:none">
<b>4. What famous comedian used to work for IBM?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) JEFF FOXWORTHY</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) TIM CONWAY</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) BRETT BUTLER</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) TIM ALLEN</a><br>
</div>
<div id="question5" style="display:none">
<b>5. What three base colors do monitors use to compose all other colors?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) WHITE, BLACK AND BLUE</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) YELLOW, CYAN AND MAGENTA</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) RED, GREEN AND BLUE</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) YELLOW, RED AND GREEN</a><br>
</div>
<div id="question6" style="display:none">
<b>6. If the battery in your desktop PC went dead, what would go wrong?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) DATE, TIME AND DATA ON ALL HARD DRIVES WOULD BE LOST.</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) COMPUTER WOULD NOT BOOT UP AND DATA ON ALL HARD DRIVES WOULD BE
LOST.</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) DATE, TIME AND ANY NON-DEFAULT BIOS SETTINGS WOULD BE LOST.
</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) THERE IS NO BATTERY IN A DESKTOP PC.
</a><br>
</div>
<div id="question7" style="display:none">
<b>7. What web development technology was developed by the Allaire Corporation?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) COLDFUSION</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) ISAPI) INTERNET SERVER APPLICATION PROGRAMMING INTERFACE</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) ACTIVE SERVER PAGES</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) CGI (COMMON GATEWAY INTERFACE)</a><br>
</div>
<div id="question8" style="display:none">
<b>8. What was the original name for the Internet?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) USANET</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) COMMNET</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) ARPANET</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) UNITED STATES COMPUTER COMMUNICATIONS SYSTEM</a><br>
</div>
<div id="question9" style="display:none">
<b>9. What does the acronym SCSI stand for?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) STANDARD CONTROLLER FOR SYSTEMS INTEGRATION</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) SOFTWARE CLIENT SERVER INTEGRATION</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) SMALL COMPUTER SYSTEMS INTERFACE</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) SECURITY CERTIFICATE SYSTEMS INTERFACE</a><br>
</div>
<div id="question10" style="display:none">
<b>10. What school did the famous 'Internet Worm' of 1989 originate from?</b><br>
<a href="javascript:void(0)" onclick="check_answer('a')">a) CARNEGIE MELLON UNIVERSITY</a><br>
<a href="javascript:void(0)" onclick="check_answer('b')">b) CORNELL UNIVERSITY</a><br>
<a href="javascript:void(0)" onclick="check_answer('c')">c) MIT</a><br>
<a href="javascript:void(0)" onclick="check_answer('d')">d) CIT</a><br>
</div>
<div id="quizScore" style="display:none">
</div>
</body>
</html>
```

