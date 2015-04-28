# Javascript OpenSimulatedExam (JOSE)
OpenSimulatedExam is a free open source sofware, it's an alternative to VCE Exam Simulator. the software is a test engine designed specifically for certification exam preparation. It allows you to create, edit, and take practice tests in an environment very similar to an actual exam.
It's using html5 and css3 and It runs on all platformes Windows, Mac, Linux, Android and IOS.

# jose Files (.josf files)
OpenExamSimulator is using .josf  files (.josf stands for Javascript Open Simulated File). 
The files are writen in JSON, and the structure is clear and simple.


### .josf file example
```
{
	"name":"Title",
	"company":"Company",
	"ref":"Exam reference number",	
	"dump":"Brain dump name",
	"author":"Author name",
	"date":"Rlease date",
	"note":"Any other comments or notes",
	"number":Number Questions,
	"link":"Download link, open repository",
	"total": Maximum score,
	"success": Required score to success,
	"questions":[
		{
			"question":"Test Question",
			"answer":["Answer1","Answer2","Answer3","Answer4"],
			"correct": Array of correct answers,
			"type":The type of the answer : radio, check or drag,
			"category":"The section"
		}
	]
}
```

# josfPlayer

### HTML 
```
<!doctype html>
<html>
<head>
  <script src="jquery.min.js"></script>
  <script src="josfPlayer.js"></script>
</head>
<body>
  <div id="body"></div>
</body>
</html>
```

### javascript 
```
  <script>
	var oes=new OpenExamSimulator();
  	$.get( "Exam1.josf", function( data ) {		  
		  oes.load("body",data);
	});
  </script>
```

# josfDesigner
### Todo ...



#Todo:
- Initial commit (Installable / online version)
- Sample files
- Documentation
- Support for other files  (.VCE, .txt, .pdf)
