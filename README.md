# HCI-practice


<HTML>
<HEAD>
<SCRIPT LANGUAGE = "Javascript">


function MessageBox (textstring){alert(textstring)}
<!-- say whatever shit you want -->

function changecolor(code){document.bgColor=code
}

function password() {
Ret = prompt('Type the word castle',"");
if(Ret=="castle") {
location = 'ch03_1.html';
} else {
alert("Please try again")
}
}

function MyWindow(message) {
//Define Date to display in local syntax
now = new Date();
LocalTime = now.toLocaleString();
//Define contents of page
contents=
'<body bgcolor="beige">'+
'<h2>Hello</h2>'+
'Click on the message below to close this window<br>'+
'<A HREF="javascript:window.close()" >'+
message +
'</A>'
//Create new Window
options =	"toolbar=0,status=0,menubar=0,scrollbars=0," +
"resizable=0,width=300,height=200";
newwindow=window.open("","mywindow", options);
newwindow.document.writeln(LocalTime);
newwindow.document.write(contents);
newwindow.document.close();
}


function getSelect(s) {
  return s.options[s.selectedIndex].value
}


function MakePage(name,town,roommate,age) {

var content = '<HTML><HEAD><TITLE>'+name+'\'s Page</title>' +
'</head><body background="images/space.gif" text="black" link="#FFBBBB" vlink="#FFBBBB">' +
'<FONT COLOR="4EEA6C"><center><h1>' +
name + '\'s Page</h1></center></FONT>' +
'<IMG ALIGN=Left SRC="http://images.webteacher.com/javascript/images/heart.gif" WIDTH="72" HEIGHT="72">Hello, and welcome to my page. I live in ' + town + ' and I am ' + age + ' years old.' +
'<p>' + town + ' isn\'t a bad place to live, if you can stand ' + roommate + '\'s cooking <P>' +
'Some people think they\'re so cool just because they created a home page. <br> ' +
'They have fancy backgrounds and colors, but they just go on and on with nothing to say. <br> ' +
'<A HREF="http://www.yahoo.com/">Click Here to search Yahoo</A><--Boy, there\'s a link I never' +
' would have found on my own. Some people\'s pages are so boring I think my computer could do' +
' a better job with a 10 line program.'

document.open("","MyWindow", options);
document.write(content)
document.close()

}

function rushbox(checked) {
if (checked==true) {alert(" LIFT OFF! ")}
}





</SCRIPT>
</HEAD>

<BODY>
<FORM>
<INPUT NAME="text1" TYPE="text">
<INPUT NAME="submit" TYPE="button" VALUE="Show Me" onClick="MessageBox(form.text1.value)">
</FORM>

<FORM>
<input type="button" name="Button1" value="RED" onclick="changecolor('red')">

<input type="button" name="Button2" value="GREEN" onclick="changecolor('green')">

<input type="button" name="Button3" value="CYAN" onclick="changecolor('4FEAD3')">

<input type="button" name="Button4" value="WHITE" onclick="changecolor('white')">

</FORM>

<A HREF="javascript:password()">
<IMG SRC="pict1.gif" NAME="pic1" ALT="about us!" BORDER="0" align="left"></A>

<H3>Click the image to enter a password protected document. Try a wrong entry first.</H3>

</BODY>

<BODY bgcolor="white" onLoad="this.form1.text1.focus()">

<TABLE BORDER=1 bgcolor="beige"><tr><td><B>Type a message in the box,<br> it will become a link to close the new window.</B>
<FORM NAME="form1">
<INPUT NAME="text1" TYPE=Text SIZE="50" MAXLENGTH="50">
<INPUT TYPE=Button VALUE="Create my window" onClick="MyWindow(form.text1.value)">
</FORM>
</TABLE>

<br>
<FORM>
<SELECT NAME="list" SIZE=1 OnChange="location=getSelect(this)">
<OPTION value="#"> Choose a search engine
<OPTION value="http://www.yahoo.com"> Yahoo
<OPTION value="http://www.google.com"> Google
<OPTION value="http://www.bing.com"> Bing
<OPTION value="http://www.ask.com"> Ask.com
<OPTION value="http://www.lycos.com"> Lycos
<OPTION value="http://www.excite.com"> Excite

</SELECT>
<br>

</FORM>

<TABLE BORDER=1 bgcolor="beige"><tr><td><B>Type a messages in the fiels below,<br> it will open a new window.</B>
<FORM NAME="form1"><tr><td> Please enter your first name
<INPUT NAME="text1" TYPE=Text SIZE="50" MAXLENGTH="50">
<FORM NAME="form1"><tr><td> What city/town do you live in?
<INPUT NAME="text1" TYPE=Text SIZE="50" MAXLENGTH="50">
<FORM NAME="form1"><tr><td> How old are you?
<INPUT NAME="text1" TYPE=Text SIZE="50" MAXLENGTH="50">
<FORM NAME="form1"><tr><td> Name another person in your house
<INPUT NAME="text1" TYPE=Text SIZE="50" MAXLENGTH="50"><br>

<INPUT TYPE=Button VALUE="Create my Home Page" onClick="MakePage(form.text1.value)">
</FORM>
</TABLE>

<br>
<br>
<FORM>
<INPUT TYPE=checkbox NAME="rush" OnClick="rushbox(form.rush.checked)"
Rush this order <FORM>
<br>
<br>


<!--
Below here the code that shows a short hi message when mousing over the "point to me" image
-->
<A HREF="#" OnMouseOver="alert('hi')">
<IMG SRC="http://images.webteacher.com/javascript/images/pointme.gif" BORDER=0 >
</A>

</BODY>



</HTML>

