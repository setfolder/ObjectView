// Function for outputting the contents of objects of any nesting
// Example of use: obv( объект [,do_recursion(true|false)] );

function obv(x,r,s,ss) {
	if (typeof x != 'object') return document.write('This is not an object');
	var s = s || "";  var ss = ss || "";  var r = r || false;
	document.write("{<br> &nbsp;");
	for (e in x)
	{
		if ( (typeof x[e] == 'object') && (r != false) )
			{ obv(x[e],"&nbsp;&nbsp;","<br>") }
		else { document.write(s+e+' : '+x[e]+"<br> &nbsp;") };
	};
	document.write("}"+ss);
};