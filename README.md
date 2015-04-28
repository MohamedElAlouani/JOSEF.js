# OpenExamSimulator
OpenExamSimulator is a free open source sofware, it's an alternative to VCE Exam Simulator. the software is a test engine designed specifically for certification exam preparation. It allows you to create, edit, and take practice tests in an environment very similar to an actual exam.
It's using html5 and css3 and It runs on all platformes Windows, Mac, Linux, Android and IOS.


# Web version

### HTML 
```
<!doctype html>
<html>
<head>
  <script src="jquery.min.js"></script>
  <script src="OpenExamSimulator.js"></script>
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
  	$.get( "exam1.oce", function( data ) {		  
		  oes.load("body",data);
	});
  </script>
```


# .oce files
OpenExamSimulator is using .oce files (.oce stands for open certification exam). 
The files are writen in JSON, and the coding is simple. (todo: more about file structure)

### .oce file example
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



#Todo:
- Initial commit (Installable / online version)
- Sample files
- Documentation
- Support for other files  (.VCE, .txt, .pdf)
