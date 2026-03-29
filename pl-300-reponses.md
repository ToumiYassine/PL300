# PL-300 - Questions Complètes, Réponses et Explications

## Question 1
**Énoncé de la question :**
HOTSPOT	-
You	plan	to	create	the	Power	BI	model	shown	in	the	exhibit.	(Click	the	Exhibit	tab.)
The	data	has	the	following	refresh	requirements:
✑
	Customer	must	be	refreshed	daily.
✑
	Date	must	be	refreshed	once	every	three	years.
✑
	Sales	must	be	refreshed	in	near	real	time.
✑
	SalesAggregate	must	be	refreshed	once	per	week.
You	need	to	select	the	storage	modes	for	the	tables.	The	solution	must	meet	the	following	requirements:
✑
	Minimize	the	load	times	of	visuals.
✑
	Ensure	that	the	data	is	loaded	to	the	model	based	on	the	refresh	requirements.
Which	storage	mode	should	you	select	for	each	table?	To	answer,	select	the	appropriate	options	in	the	answer
area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:	Dual	-
Customer	should	use	the	dual	storage	mode.
Dual:	Tables	with	this	setting	can	act	as	either	cached	or	not	cached,	depending	on	the	context	of	the	query
that's	submitted	to	the	Power	BI	dataset.	In	some	cases,	you	fulfill	queries	from	cached	data.	In	other	cases,
you	fulfill	queries	by	executing	an	on-demand	query	to	the	data	source.
Note:	You	set	the	Storage	mode	property	to	one	of	these	three	values:	Import,	DirectQuery,	and	Dual.
Box	2:	Dual	-
You	can	set	the	dimension	tables	(Customer,	Geography,	and	Date)	to	Dual	to	reduce	the	number	of	limited
relationships	in	the	dataset,	and	improve	performance.
Box	3:	DirectQuery	-
Sales	should	use	the	DirectQuery	storage	mode.
DirectQuery:	Tables	with	this	setting	aren't	cached.	Queries	that	you	submit	to	the	Power	BI	dataset"for
example,	DAX	queries"and	that	return	data	from
DirectQuery	tables	can	be	fulfilled	only	by	executing	on-demand	queries	to	the	data	source.	Queries	that	you
submit	to	the	data	source	use	the	query	language	for	that	data	source,	for	example,	SQL.
Box	4:	Import	-
Import:	Imported	tables	with	this	setting	are	cached.	Queries	submitted	to	the	Power	BI	dataset	that	return
data	from	Import	tables	can	be	fulfilled	only	from	cached	data.
Note:-
Dual	(Composite)	Mode:
The	dual	storage	mode	is	between	Import	and	DirectQuery.	it	is	a	hybrid	approach,	Like	importing	data,	the
dual	storage	mode	caches	the	data	in	the	table.	However,	it	leaves	it	up	to	Power	BI	to	determine	the	best	way
to	query	the	table	depending	on	the	query	context.
1)	Sales	Must	be	Refreshed	in	Near	real	time	so	"Direct	Query"
2)	Sales	Aggregate	is	once	per	week	so	"Import"	(performance	also	required)
3)	Both	Date	and	Customer	has	relationship	with	both	Sales	and	SalesAggregate	tables	so	"Dual"
because	to	support	performance	for	DirectQuery(Sales)	and	Import(SalesAggregate)
Reference:
https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-storage-mode
You	have	a	project	management	app	that	is	fully	hosted	in	Microsoft	Teams.	The	app	was	developed	by	using
Microsoft	Power	Apps.
You	need	to	create	a	Power	BI	report	that	connects	to	the	project	management	app.
Which	connector	should	you	select?
A.	
Microsoft	Teams	Personal	Analytics
B.	
SQL	Server	database
C.	
Dataverse
D.	
Dataflows
Answer:	
C
Explanation:
Data	sources	in	Power	BI	Desktop.
The	Power	Platform	category	provides	the	following	data	connections:
Power	BI	datasets	-
Power	BI	dataflows	-

---

## Question 2
**Énoncé de la question :**
You	have	a	project	management	app	that	is	fully	hosted	in	Microsoft	Teams.	The	app	was	developed	by	using
Microsoft	Power	Apps.
You	need	to	create	a	Power	BI	report	that	connects	to	the	project	management	app.
Which	connector	should	you	select?
A.	
Microsoft	Teams	Personal	Analytics
B.	
SQL	Server	database
C.	
Dataverse
D.	
Dataflows
Answer:	
C
Explanation:
Data	sources	in	Power	BI	Desktop.
The	Power	Platform	category	provides	the	following	data	connections:
Power	BI	datasets	-
Power	BI	dataflows	-

**Réponse exacte :**
A

**Explication courte :**
Power	BI	dataset
because	the	case	states	there	is	already	a	report	published	and	the	datamodel	contains	measures.	therefore
and	to	be	able	to	use	the	measures	in	the	datamodel	you	should	connect	to	the	existing	dataset	(which	was
created	when	you	plublished	the	report)	instead	of	starting	from	scratch	with	the	files	in	the	SharePoint
folder.
You	import	two	Microsoft	Excel	tables	named	Customer	and	Address	into	Power	Query.	Customer	contains	the
following	columns:
✑
	Customer	ID
✑
	Customer	Name
✑
	Phone
✑
	Email	Address
✑
	Address	ID
Address	contains	the	following	columns:
✑
	Address	ID
✑
	Address	Line	1
✑
	Address	Line	2

---

## Question 4
**Énoncé de la question :**
Power	BI	dataset
because	the	case	states	there	is	already	a	report	published	and	the	datamodel	contains	measures.	therefore
and	to	be	able	to	use	the	measures	in	the	datamodel	you	should	connect	to	the	existing	dataset	(which	was
created	when	you	plublished	the	report)	instead	of	starting	from	scratch	with	the	files	in	the	SharePoint
folder.
You	import	two	Microsoft	Excel	tables	named	Customer	and	Address	into	Power	Query.	Customer	contains	the
following	columns:
✑
	Customer	ID
✑
	Customer	Name
✑
	Phone
✑
	Email	Address
✑
	Address	ID
Address	contains	the	following	columns:
✑
	Address	ID
✑
	Address	Line	1
✑
	Address	Line	2

**Réponse exacte :**
A

**Explication courte :**
Remember	Merge	is	JOIN,	APPEND	is	UNION
A	merge	queries	operation	joins	two	existing	tables	together	based	on	matching	values	from	one	or	multiple
columns.	You	can	choose	to	use	different	types	of	joins,	depending	on	the	output	you	want.
Reference:
https://docs.microsoft.com/en-us/power-query/merge-queries-overview

---

## Question 5
**Énoncé de la question :**
HOTSPOT	-
You	have	two	Azure	SQL	databases	that	contain	the	same	tables	and	columns.
For	each	database,	you	create	a	query	that	retrieves	data	from	a	table	named	Customer.
You	need	to	combine	the	Customer	tables	into	a	single	table.	The	solution	must	minimize	the	size	of	the	data	model
and	support	scheduled	refresh	in	powerbi.com.
What	should	you	do?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:	
Append	Queries	as	New	-
When	you	have	additional	rows	of	data	that	you'd	like	to	add	to	an	existing	query,	you	append	the	query.
There	are	two	append	options:
*	Append	queries	as	new	displays	the	Append	dialog	box	to	create	a	new	query	by	appending	multiple	tables.
*	Append	queries	displays	the	Append	dialog	box	to	add	additional	tables	to	the	current	query.
Incorrect:	When	you	have	one	or	more	columns	that	you'd	like	to	add	to	another	query,	you	merge	the	queries.
Box	2:	
Disable	loading	the	query	to	the	data	model
By	default,	all	queries	from	Query	Editor	will	be	loaded	into	the	memory	of	Power	BI	Model.	You	can	disable
the	load	for	some	queries,	especially	queries	that	used	as	intermediate	transformation	to	produce	the	final
query	for	the	model.
Disabling	Load	doesn't	mean	the	query	won't	be	refreshed,	it	only	means	the	query	won't	be	loaded	into	the
memory.	When	you	click	on	Refresh	model	in	Power
BI,	or	when	a	scheduled	refresh	happens	even	queries	marked	as	Disable	Load	will	be	refreshed,	but	their
data	will	be	used	as	intermediate	source	for	other	queries	instead	of	loading	directly	into	the	model.	This	is	a
very	basic	performance	tuning	tip,	but	very	important	when	your	Power	BI	model	grows	bigger	and	bigger.
Reference:
https://docs.microsoft.com/en-us/power-query/append-queries
https://radacad.com/performance-tip-for-power-bi-enable-load-sucks-memory-up
DRAG	DROP	-
In	Power	Query	Editor,	you	have	three	queries	named	ProductCategory,	ProductSubCategory,	and	Product.
Every	Product	has	a	ProductSubCategory.
Not	every	ProductsubCategory	has	a	parent	ProductCategory.
You	need	to	merge	the	three	queries	into	a	single	query.	The	solution	must	ensure	the	best	performance	in	Power
Query.
How	should	you	merge	the	tables?	To	answer,	drag	the	appropriate	merge	types	to	the	correct	queries.	Each
merge	type	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between	panes	or
scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:

---

## Question 6
**Énoncé de la question :**
https://radacad.com/performance-tip-for-power-bi-enable-load-sucks-memory-up
DRAG	DROP	-
In	Power	Query	Editor,	you	have	three	queries	named	ProductCategory,	ProductSubCategory,	and	Product.
Every	Product	has	a	ProductSubCategory.
Not	every	ProductsubCategory	has	a	parent	ProductCategory.
You	need	to	merge	the	three	queries	into	a	single	query.	The	solution	must	ensure	the	best	performance	in	Power
Query.
How	should	you	merge	the	tables?	To	answer,	drag	the	appropriate	merge	types	to	the	correct	queries.	Each
merge	type	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between	panes	or
scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:

**Réponse exacte :**


**Explication courte :**
Box	1:	Inner	-
Every	Product	has	a	ProductSubCategory.
A	standard	join	is	needed.
One	of	the	join	kinds	available	in	the	Merge	dialog	box	in	Power	Query	is	an	inner	join,	which	brings	in	only
matching	rows	from	both	the	left	and	right	tables.
Box	2:	Left	outer	-
Not	every	ProductsubCategory	has	a	parent	ProductCategory.
One	of	the	join	kinds	available	in	the	Merge	dialog	box	in	Power	Query	is	a	left	outer	join,	which	keeps	all	the
rows	from	the	left	table	and	brings	in	any	matching	rows	from	the	right	table.
Reference:
https://docs.microsoft.com/en-us/power-query/merge-queries-inner	https://docs.microsoft.com/en-us/power-
query/merge-queries-left-outer
You	are	building	a	Power	BI	report	that	uses	data	from	an	Azure	SQL	database	named	erp1.
You	import	the	following	tables.
You	need	to	perform	the	following	analyses:
✑
	Orders	sold	over	time	that	include	a	measure	of	the	total	order	value
Orders	by	attributes	of	products	sold
The	solution	must	minimize	update	times	when	interacting	with	visuals	in	the	report.
What	should	you	do	first?
A.	
From	Power	Query,	merge	the	Order	Line	Items	query	and	the	Products	query.
B.	
Create	a	calculated	column	that	adds	a	list	of	product	categories	to	the	Orders	table	by	using	a	DAX
function.
C.	
Calculate	the	count	of	orders	per	product	by	using	a	DAX	function.
D.	
From	Power	Query,	merge	the	Orders	query	and	the	Order	Line	Items	query.
Answer:	
D
Explanation:
	D.	It's	the	Header/Detail	Schema,	and	the	most	optimal	way	is	to	flatten	the	header	into	the	detail	table.
Source:
https://www.sqlbi.com/articles/header-detail-vs-star-schema-models-in-tabular-and-power-bi/
GPT:	Merging	the	Orders	query	and	the	Order	Line	Items	query	in	Power	Query	will	allow	you	to	create	a
single	query	that	combines	the	necessary	data	from	the	different	tables.	This	will	make	it	easier	and	more
efficient	to	perform	the	required	analyses,	as	you	will	have	all	the	information	you	need	in	one	place.
---	PBI	will	do	the	best	aggregation	base	on	Star	Schema	model,	we	now	have	1	Fact	table	(Order	Line	Items)
and	2	Dim	tables	(Products,	Orders).	Orders	has	common	field	with	Products	(ProductID),	and	pretty	sure	time

---

## Question 7
**Énoncé de la question :**
https://docs.microsoft.com/en-us/power-
query/merge-queries-left-outer
You	are	building	a	Power	BI	report	that	uses	data	from	an	Azure	SQL	database	named	erp1.
You	import	the	following	tables.
You	need	to	perform	the	following	analyses:
✑
	Orders	sold	over	time	that	include	a	measure	of	the	total	order	value
Orders	by	attributes	of	products	sold
The	solution	must	minimize	update	times	when	interacting	with	visuals	in	the	report.
What	should	you	do	first?
A.	
From	Power	Query,	merge	the	Order	Line	Items	query	and	the	Products	query.
B.	
Create	a	calculated	column	that	adds	a	list	of	product	categories	to	the	Orders	table	by	using	a	DAX
function.
C.	
Calculate	the	count	of	orders	per	product	by	using	a	DAX	function.
D.	
From	Power	Query,	merge	the	Orders	query	and	the	Order	Line	Items	query.
Answer:	
D
Explanation:
	D.	It's	the	Header/Detail	Schema,	and	the	most	optimal	way	is	to	flatten	the	header	into	the	detail	table.
Source:
https://www.sqlbi.com/articles/header-detail-vs-star-schema-models-in-tabular-and-power-bi/
GPT:	Merging	the	Orders	query	and	the	Order	Line	Items	query	in	Power	Query	will	allow	you	to	create	a
single	query	that	combines	the	necessary	data	from	the	different	tables.	This	will	make	it	easier	and	more
efficient	to	perform	the	required	analyses,	as	you	will	have	all	the	information	you	need	in	one	place.
---	PBI	will	do	the	best	aggregation	base	on	Star	Schema	model,	we	now	have	1	Fact	table	(Order	Line	Items)
and	2	Dim	tables	(Products,	Orders).	Orders	has	common	field	with	Products	(ProductID),	and	pretty	sure	time

**Réponse exacte :**
A

**Explication courte :**
We	have	to	import	Excel	files	from	SharePoint,	so	we	need	the	connector	SharePoint	folder	which	is	used	to
get	access	to	the	files	stored	in	the	library.	SharePoint	list	is	a	collection	of	content	that	has	rows	and
columns	(like	a	table)	and	is	used	for	task	lists,	calendars,	etc.
Since	we	have	to	filter	only	on	manufacturing	reports,	we	have	to	select	Transform	and	then	filter	by	the
corresponding	folder	path.
DRAG	DROP	-
You	have	a	Microsoft	Excel	workbook	that	contains	two	sheets	named	Sheet1	and	Sheet2.
Sheet1	contains	the	following	table	named	Table1.
Sheet2	contains	the	following	table	named	Table2.

---

## Question 9
**Énoncé de la question :**
We	have	to	import	Excel	files	from	SharePoint,	so	we	need	the	connector	SharePoint	folder	which	is	used	to
get	access	to	the	files	stored	in	the	library.	SharePoint	list	is	a	collection	of	content	that	has	rows	and
columns	(like	a	table)	and	is	used	for	task	lists,	calendars,	etc.
Since	we	have	to	filter	only	on	manufacturing	reports,	we	have	to	select	Transform	and	then	filter	by	the
corresponding	folder	path.
DRAG	DROP	-
You	have	a	Microsoft	Excel	workbook	that	contains	two	sheets	named	Sheet1	and	Sheet2.
Sheet1	contains	the	following	table	named	Table1.
Sheet2	contains	the	following	table	named	Table2.

**Réponse exacte :**


**Explication courte :**
Import	From	Excel	since	it	has	not	been	loaded	to	Powerbi	initially
Append	Table	2	to	Table	1
Remove	Duplicates	from	the	table	appended	to	(Table1)
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-shape-and-combine-data
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.	
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column	and	set	the	data	type	of	the
new	column	to	Date.
B.	
Change	the	data	type	of	the	Logged	column	to	Date.
C.	
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.	
Apply	a	transformation	to	extract	the	first	11	characters	of	the	Logged	column.
Answer:	
C
Explanation:
You	should	split	the	Logged	column	by	using	"at"	as	the	delimiter.	This	will	allow	you	to	separate	the	date	and
time	into	separate	columns,	which	will	enable	you	to	analyze	the	complaints	by	date	and	use	a	built-in	date
hierarchy.	Alternatively,	you	could	also	use	a	transformation	to	extract	the	date	and	time	from	the	Logged
column	and	set	the	data	type	of	the	new	columns	to	Date	and	Time,	respectively.	Option	A	is	incorrect
because	it	only	extracts	the	last	11	characters	of	the	Logged	column,	which	would	not	include	the	date.	Option
B	is	incorrect	because	the	data	in	the	Logged	column	is	in	a	non-standard	date	format	and	cannot	be	directly
converted	to	the	Date	data	type.	Option	D	is	incorrect	because	it	only	extracts	the	first	11	characters	of	the
Logged	column,	which	would	not	include	the	time.
You	have	a	Microsoft	Excel	file	in	a	Microsoft	OneDrive	folder.
The	file	must	be	imported	to	a	Power	BI	dataset.
You	need	to	ensure	that	the	dataset	can	be	refreshed	in	powerbi.com.
Which	two	connectors	can	you	use	to	connect	to	the	file?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Excel	Workbook
B.	
Text/CSV
C.	
Folder
D.	
SharePoint	folder
E.	
Web
Answer:	
DE
Explanation:
We	can	import	an	excel	file	from	multiple	connectors	(excel	workbook,	folder,	web,	share	point)	but	if	we	must
refresh	the	data	from	the	service	with	no	gateways	then	We	must	use	web	and	share	point	connectors.

---

## Question 13
**Énoncé de la question :**
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.	
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column	and	set	the	data	type	of	the
new	column	to	Date.
B.	
Change	the	data	type	of	the	Logged	column	to	Date.
C.	
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.	
Apply	a	transformation	to	extract	the	first	11	characters	of	the	Logged	column.
Answer:	
C
Explanation:
You	should	split	the	Logged	column	by	using	"at"	as	the	delimiter.	This	will	allow	you	to	separate	the	date	and
time	into	separate	columns,	which	will	enable	you	to	analyze	the	complaints	by	date	and	use	a	built-in	date
hierarchy.	Alternatively,	you	could	also	use	a	transformation	to	extract	the	date	and	time	from	the	Logged
column	and	set	the	data	type	of	the	new	columns	to	Date	and	Time,	respectively.	Option	A	is	incorrect
because	it	only	extracts	the	last	11	characters	of	the	Logged	column,	which	would	not	include	the	date.	Option
B	is	incorrect	because	the	data	in	the	Logged	column	is	in	a	non-standard	date	format	and	cannot	be	directly
converted	to	the	Date	data	type.	Option	D	is	incorrect	because	it	only	extracts	the	first	11	characters	of	the
Logged	column,	which	would	not	include	the	time.
You	have	a	Microsoft	Excel	file	in	a	Microsoft	OneDrive	folder.
The	file	must	be	imported	to	a	Power	BI	dataset.
You	need	to	ensure	that	the	dataset	can	be	refreshed	in	powerbi.com.
Which	two	connectors	can	you	use	to	connect	to	the	file?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Excel	Workbook
B.	
Text/CSV
C.	
Folder
D.	
SharePoint	folder
E.	
Web
Answer:	
DE
Explanation:
We	can	import	an	excel	file	from	multiple	connectors	(excel	workbook,	folder,	web,	share	point)	but	if	we	must
refresh	the	data	from	the	service	with	no	gateways	then	We	must	use	web	and	share	point	connectors.

**Réponse exacte :**


**Explication courte :**
Box	1:	Merge	-
There	are	two	primary	ways	of	combining	queries:	merging	and	appending.
*	When	you	have	one	or	more	columns	that	you'd	like	to	add	to	another	query,	you	merge	the	queries.
*	When	you	have	additional	rows	of	data	that	you'd	like	to	add	to	an	existing	query,	you	append	the	query.
Box	2:	Disable	the	query	load	-
Managing	loading	of	queries	-
In	many	situations,	it	makes	sense	to	break	down	your	data	transformations	in	multiple	queries.	One	popular
example	is	merging	where	you	merge	two	queries	into	one	to	essentially	do	a	join.	In	this	type	of	situations,
some	queries	are	not	relevant	to	load	into	Desktop	as	they	are	intermediate	steps,	while	they	are	still	required
for	your	data	transformations	to	work	correctly.	For	these	queries,	you	can	make	sure	they	are	not	loaded	in
Desktop	by	un-checking	'Enable	load'	in	the	context	menu	of	the	query	in	Desktop	or	in	the	Properties	screen:
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-shape-and-combine-data	https://docs.micr
osoft.com/en-us/power-bi/connect-data/refresh-include-in-report-refresh
You	have	an	Azure	SQL	database	that	contains	sales	transactions.	The	database	is	updated	frequently.
You	need	to	generate	reports	from	the	data	to	detect	fraudulent	transactions.	The	data	must	be	visible	within	five
minutes	of	an	update.
How	should	you	configure	the	data	connection?

---

## Question 14
**Énoncé de la question :**
https://docs.micr
osoft.com/en-us/power-bi/connect-data/refresh-include-in-report-refresh
You	have	an	Azure	SQL	database	that	contains	sales	transactions.	The	database	is	updated	frequently.
You	need	to	generate	reports	from	the	data	to	detect	fraudulent	transactions.	The	data	must	be	visible	within	five
minutes	of	an	update.
How	should	you	configure	the	data	connection?

**Réponse exacte :**
D

**Explication courte :**
DirectQuery:	No	data	is	imported	or	copied	into	Power	BI	Desktop.	For	relational	sources,	the	selected	tables
and	columns	appear	in	the	Fields	list.	For	multi-	dimensional	sources	like	SAP	Business	Warehouse,	the
dimensions	and	measures	of	the	selected	cube	appear	in	the	Fields	list.	As	you	create	or	interact	with	a
visualization,	Power	BI	Desktop	queries	the	underlying	data	source,	so	you're	always	viewing	current	data.
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-use-directquery
DRAG	DROP	-
You	have	a	folder	that	contains	100	CSV	files.
You	need	to	make	the	file	metadata	available	as	a	single	dataset	by	using	Power	BI.	The	solution	must	NOT	store
the	data	of	the	CSV	files.
Which	three	actions	should	you	perform	in	sequence.	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
1.	Get	data	and	select	folder
2.	Remove	the	content	column
3.	Expand	the	attributes	column
A	business	intelligence	(BI)	developer	creates	a	dataflow	in	Power	BI	that	uses	DirectQuery	to	access	tables	from
an	on-premises	Microsoft	SQL	server.	The

---

## Question 16
**Énoncé de la question :**
DRAG	DROP	-
You	have	a	folder	that	contains	100	CSV	files.
You	need	to	make	the	file	metadata	available	as	a	single	dataset	by	using	Power	BI.	The	solution	must	NOT	store
the	data	of	the	CSV	files.
Which	three	actions	should	you	perform	in	sequence.	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
1.	Get	data	and	select	folder
2.	Remove	the	content	column
3.	Expand	the	attributes	column
A	business	intelligence	(BI)	developer	creates	a	dataflow	in	Power	BI	that	uses	DirectQuery	to	access	tables	from
an	on-premises	Microsoft	SQL	server.	The

**Réponse exacte :**
C

**Explication courte :**
A	daily	update	is	adequate.
When	you	set	up	a	refresh	schedule,	Power	BI	connects	directly	to	the	data	sources	using	connection
information	and	credentials	in	the	dataset	to	query	for	updated	data,	then	loads	the	updated	data	into	the
dataset.	Any	visualizations	in	reports	and	dashboards	based	on	that	dataset	in	the	Power	BI	service	are	also
updated.
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/refresh-desktop-file-local-drive
DRAG	DROP
-
You	publish	a	dataset	that	contains	data	from	an	on-premises	Microsoft	SQL	Server	database.
The	dataset	must	be	refreshed	daily.
You	need	to	ensure	that	the	Power	BI	service	can	connect	to	the	database	and	refresh	the	dataset.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.

---

## Question 17
**Énoncé de la question :**
DRAG	DROP
-
You	publish	a	dataset	that	contains	data	from	an	on-premises	Microsoft	SQL	Server	database.
The	dataset	must	be	refreshed	daily.
You	need	to	ensure	that	the	Power	BI	service	can	connect	to	the	database	and	refresh	the	dataset.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.

**Réponse exacte :**


**Explication courte :**
Configure	an	on	premises	data	gateway.
Add	a	data	source.
Add	the	dataset	owner	to	the	data	source.
Configure	a	scheduled	refresh.
You	attempt	to	connect	Power	BI	Desktop	to	a	Cassandra	database.
From	the	Get	Data	connector	list,	you	discover	that	there	is	no	specific	connector	for	the	Cassandra	database.
You	need	to	select	an	alternate	data	connector	that	will	connect	to	the	database.
Which	type	of	connector	should	you	choose?
A.	
Microsoft	SQL	Server	database
B.	
ODBC
C.	
OLE	DB
D.	
OData
Answer:	
B
Explanation:
B	is	Correct	because,	B´cause	it	allows	you	to	connect	to	data	sources	that	aren't	identified	in	the	Get	Data
lists.
The	ODBC	connector	lets	you	import	data	from	any	third-party	ODBC	driver	simply	by	specifying	a	Data
Source	Name	(DSN)	or	a	connection	string.	As	an	option,	you	can	also	specify	a	SQL	statement	to	execute
against	the	ODBC	driver.
List	details	a	few	examples	of	data	sources	to	which	Power	BI	Desktop	can	connect	by	using	the	generic
ODBC	interface:
https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connect-using-generic-interfaces
DRAG	DROP
-
You	receive	annual	sales	data	that	must	be	included	in	Power	BI	reports.
From	Power	Query	Editor,	you	connect	to	the	Microsoft	Excel	source	shown	in	the	following	exhibit.

---

## Question 19
**Énoncé de la question :**
DRAG	DROP
-
You	receive	annual	sales	data	that	must	be	included	in	Power	BI	reports.
From	Power	Query	Editor,	you	connect	to	the	Microsoft	Excel	source	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Select	the	Month	and	Month	Number	Columns.
Select	Unpivot	Other	Columns
Rename	the	Attribute	Column	as	Year	and	the	value	Column	as	Sales.

---

## Question 20
**Énoncé de la question :**
Select	the	Month	and	Month	Number	Columns.
Select	Unpivot	Other	Columns
Rename	the	Attribute	Column	as	Year	and	the	value	Column	as	Sales.
HOTSPOT
-
You	are	using	Power	BI	Desktop	to	connect	to	an	Azure	SQL	database.
The	connection	is	configured	as	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
10	minutes.
Only	tables	that	Contain	data.

---

## Question 21
**Énoncé de la question :**
10	minutes.
Only	tables	that	Contain	data.
HOTSPOT
-
You	have	the	Azure	SQL	databases	shown	in	the	following	table.
You	plan	to	build	a	single	PBIX	file	to	meet	the	following	requirements:
•	Data	must	be	consumed	from	the	database	that	corresponds	to	each	stage	of	the	development	lifecycle.
•	Power	BI	deployment	pipelines	must	NOT	be	used.
•	The	solution	must	minimize	administrative	effort.
What	should	you	do?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
To	meet	the	requirements	specified,	we	can	use	a	single	parameter	in	the	PBIX	file	that	controls	which
database	is	used	for	data	consumption	based	on	the	stage	of	the	development	lifecycle.
We	can	use	a	Text	parameter	type	in	Power	BI	to	achieve	this.	The	parameter	can	be	used	to	switch	between
the	different	database	connections	when	a	user	interacts	with	the	report.	The	text	parameter	could	include
values	such	as	"Development",	"Staging",	and	"Production",	which	correspond	to	the	different	databases
shown	in	the	table.
The	parameter	can	then	be	used	in	the	queries	to	dynamically	filter	the	data	based	on	the	selected	stage	of
the	development	lifecycle.	By	using	a	single	parameter,	we	can	minimize	administrative	effort	and	ensure	that
the	report	works	with	each	stage	of	the	development	lifecycle.
You	are	creating	a	query	to	be	used	as	a	Country	dimension	in	a	star	schema.
A	snapshot	of	the	source	data	is	shown	in	the	following	table.
You	need	to	create	the	dimension.	The	dimension	must	contain	a	list	of	unique	countries.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
	Delete	the	Country	column.
B.
	Remove	duplicates	from	the	table.
C.
	Remove	duplicates	from	the	City	column.
D.
	Delete	the	City	column.
E.
	Remove	duplicates	from	the	Country	column.
Answer:	
DE
Explanation:
The	table	has	to	contain	unique	values	for	"Country"	column,	so-	delete	the	city	column	-->	in	fact	this	column
is	not	even	requested-	Remove	dupicates	from	the	Country	column
DRAG	DROP
-

---

## Question 23
**Énoncé de la question :**
To	meet	the	requirements	specified,	we	can	use	a	single	parameter	in	the	PBIX	file	that	controls	which
database	is	used	for	data	consumption	based	on	the	stage	of	the	development	lifecycle.
We	can	use	a	Text	parameter	type	in	Power	BI	to	achieve	this.	The	parameter	can	be	used	to	switch	between
the	different	database	connections	when	a	user	interacts	with	the	report.	The	text	parameter	could	include
values	such	as	"Development",	"Staging",	and	"Production",	which	correspond	to	the	different	databases
shown	in	the	table.
The	parameter	can	then	be	used	in	the	queries	to	dynamically	filter	the	data	based	on	the	selected	stage	of
the	development	lifecycle.	By	using	a	single	parameter,	we	can	minimize	administrative	effort	and	ensure	that
the	report	works	with	each	stage	of	the	development	lifecycle.
You	are	creating	a	query	to	be	used	as	a	Country	dimension	in	a	star	schema.
A	snapshot	of	the	source	data	is	shown	in	the	following	table.
You	need	to	create	the	dimension.	The	dimension	must	contain	a	list	of	unique	countries.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
	Delete	the	Country	column.
B.
	Remove	duplicates	from	the	table.
C.
	Remove	duplicates	from	the	City	column.
D.
	Delete	the	City	column.
E.
	Remove	duplicates	from	the	Country	column.
Answer:	
DE
Explanation:
The	table	has	to	contain	unique	values	for	"Country"	column,	so-	delete	the	city	column	-->	in	fact	this	column
is	not	even	requested-	Remove	dupicates	from	the	Country	column
DRAG	DROP
-

**Réponse exacte :**


**Explication courte :**
Select	the	discount	Column
Select	Replace	Errors	to	replace	each	error	value	with	0.05
For	the	discount	column	,Change	Data	Type	to	Decimal	Number.

---

## Question 24
**Énoncé de la question :**
Select	the	discount	Column
Select	Replace	Errors	to	replace	each	error	value	with	0.05
For	the	discount	column	,Change	Data	Type	to	Decimal	Number.
HOTSPOT
-
You	attempt	to	use	Power	Query	Editor	to	create	a	custom	column	and	receive	the	error	message	shown	in	the
following	exhibit.
Use	the	drop-down	menus	to	select	the	answer	choice	that	completes	each	statement	based	on	the	information
presented	in	the	graphic.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

**Réponse exacte :**


**Explication courte :**
mismatched	data	types
A1
From	Power	Query	Editor,	you	attempt	to	execute	a	query	and	receive	the	following	error	message.
Datasource.Error:	Could	not	find	file.
What	are	two	possible	causes	of	the	error?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
You	do	not	have	permissions	to	the	file.
B.
An	incorrect	privacy	level	was	used	for	the	data	source.
C.
The	file	is	locked.
D.
The	referenced	file	was	moved	to	a	new	location.
Answer:	
AD
Explanation:
A	and	D.	A	if	PBI	cant	find	the	file	in	the	given	path	and	D	due	this.
https://community.fabric.microsoft.com/t5/Power-Query/SOLVED-Datasource-error-could-not-find-file/td-
p/252703
You	have	data	in	a	Microsoft	Excel	worksheet	as	shown	in	the	following	table.

---

## Question 26
**Énoncé de la question :**
p/252703
You	have	data	in	a	Microsoft	Excel	worksheet	as	shown	in	the	following	table.

**Réponse exacte :**
A

**Explication courte :**
A.	Select	Replace	Errors	-	is	correct.	C&D	will	remove	some	rows	Option	B,	"Edit	the	query	in	the	Query	Errors
group",	would	technically	also	allow	to	achieve	the	required	result.	However,	this	would	not	be	the	optimal
solution	given	the	constraints	provided	in	the	scenario,	which	specifies	that	administrative	effort	must	be
minimized.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Apply	the	Parse	function	from	the	Data	transformations	options	to	the	Logged	column.
B.
Change	the	data	type	of	the	Logged	column	to	Date.
C.
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.
Create	a	column	by	example	that	starts	with	2018-12-31.
Answer:	
C
Explanation:
Split	the	Logged	column	by	using	at	as	the	delimiter.
You	should	split	the	Logged	column	by	using	"at"	as	the	delimiter.	This	will	allow	you	to	separate	the	date	and
time	into	separate	columns,	which	will	enable	you	to	analyze	the	complaints	by	date	and	use	a	built-in	date
hierarchy.	Alternatively,	you	could	also	use	a	transformation	to	extract	the	date	and	time	from	the	Logged
column	and	set	the	data	type	of	the	new	columns	to	Date	and	Time,	respectively.	Option	A	is	incorrect
because	it	only	extracts	the	last	11	characters	of	the	Logged	column,	which	would	not	include	the	date.	Option
B	is	incorrect	because	the	data	in	the	Logged	column	is	in	a	non-standard	date	format	and	cannot	be	directly
converted	to	the	Date	data	type.	Option	D	is	incorrect	because	it	only	extracts	the	first	11	characters	of	the
Logged	column,	which	would	not	include	the	time.
DRAG	DROP
-
You	have	two	Microsoft	Excel	workbooks	in	a	Microsoft	OneDrive	folder.
Each	workbook	contains	a	table	named	Sales.	The	tables	have	the	same	data	structure	in	both	workbooks.
You	plan	to	use	Power	BI	to	combine	both	Sales	tables	into	a	single	table	and	create	visuals	based	on	the	data	in
the	table.	The	solution	must	ensure	that	you	can	publish	a	separate	report	and	dataset.
Which	storage	mode	should	you	use	for	the	report	file	and	the	dataset	file?	To	answer,	drag	the	appropriate	modes
to	the	correct	files.	Each	mode	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.

---

## Question 28
**Énoncé de la question :**
A.	Select	Replace	Errors	-	is	correct.	C&D	will	remove	some	rows	Option	B,	"Edit	the	query	in	the	Query	Errors
group",	would	technically	also	allow	to	achieve	the	required	result.	However,	this	would	not	be	the	optimal
solution	given	the	constraints	provided	in	the	scenario,	which	specifies	that	administrative	effort	must	be
minimized.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Apply	the	Parse	function	from	the	Data	transformations	options	to	the	Logged	column.
B.
Change	the	data	type	of	the	Logged	column	to	Date.
C.
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.
Create	a	column	by	example	that	starts	with	2018-12-31.
Answer:	
C
Explanation:
Split	the	Logged	column	by	using	at	as	the	delimiter.
You	should	split	the	Logged	column	by	using	"at"	as	the	delimiter.	This	will	allow	you	to	separate	the	date	and
time	into	separate	columns,	which	will	enable	you	to	analyze	the	complaints	by	date	and	use	a	built-in	date
hierarchy.	Alternatively,	you	could	also	use	a	transformation	to	extract	the	date	and	time	from	the	Logged
column	and	set	the	data	type	of	the	new	columns	to	Date	and	Time,	respectively.	Option	A	is	incorrect
because	it	only	extracts	the	last	11	characters	of	the	Logged	column,	which	would	not	include	the	date.	Option
B	is	incorrect	because	the	data	in	the	Logged	column	is	in	a	non-standard	date	format	and	cannot	be	directly
converted	to	the	Date	data	type.	Option	D	is	incorrect	because	it	only	extracts	the	first	11	characters	of	the
Logged	column,	which	would	not	include	the	time.
DRAG	DROP
-
You	have	two	Microsoft	Excel	workbooks	in	a	Microsoft	OneDrive	folder.
Each	workbook	contains	a	table	named	Sales.	The	tables	have	the	same	data	structure	in	both	workbooks.
You	plan	to	use	Power	BI	to	combine	both	Sales	tables	into	a	single	table	and	create	visuals	based	on	the	data	in
the	table.	The	solution	must	ensure	that	you	can	publish	a	separate	report	and	dataset.
Which	storage	mode	should	you	use	for	the	report	file	and	the	dataset	file?	To	answer,	drag	the	appropriate	modes
to	the	correct	files.	Each	mode	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
Report	file:	Import.
In	Power	BI,	when	you	import	data,	it	means	that	the	data	is	loaded	into	the	Power	BI	Desktop	file.	In	this	case,
you	would	import	the	data	from	both	Excel	workbooks	into	your	Power	BI	Desktop	report	file.	This	allows	you
to	create	visuals	and	reports	based	on	the	imported	data.	Importing	the	data	ensures	that	you	can	work	with
the	data	even	when	you're	not	connected	to	OneDrive.
Dataset:	Direct	Query.
To	keep	the	data	in	OneDrive	and	maintain	a	live	connection	to	the	source,	you	should	use	Direct	Query	for	the
dataset.	Direct	Query	allows	Power	BI	to	retrieve	and	query	data	from	the	original	data	source	(in	this	case,
the	Excel	workbooks	in	OneDrive)	in	real-time	without	importing	it	into	the	dataset.	This	ensures	that	your
dataset	is	always	up-to-date	and	reflects	changes	made	to	the	source	data.
You	use	Power	Query	to	import	two	tables	named	Order	Header	and	Order	Details	from	an	Azure	SQL	database.
The	Order	Header	table	relates	to	the	Order	Details	table	by	using	a	column	named	Order	ID	in	each	table.
You	need	to	combine	the	tables	into	a	single	query	that	contains	the	unique	columns	of	each	table.
What	should	you	select	in	Power	Query	Editor?
A.
Merge	queries

---

## Question 29
**Énoncé de la question :**
Report	file:	Import.
In	Power	BI,	when	you	import	data,	it	means	that	the	data	is	loaded	into	the	Power	BI	Desktop	file.	In	this	case,
you	would	import	the	data	from	both	Excel	workbooks	into	your	Power	BI	Desktop	report	file.	This	allows	you
to	create	visuals	and	reports	based	on	the	imported	data.	Importing	the	data	ensures	that	you	can	work	with
the	data	even	when	you're	not	connected	to	OneDrive.
Dataset:	Direct	Query.
To	keep	the	data	in	OneDrive	and	maintain	a	live	connection	to	the	source,	you	should	use	Direct	Query	for	the
dataset.	Direct	Query	allows	Power	BI	to	retrieve	and	query	data	from	the	original	data	source	(in	this	case,
the	Excel	workbooks	in	OneDrive)	in	real-time	without	importing	it	into	the	dataset.	This	ensures	that	your
dataset	is	always	up-to-date	and	reflects	changes	made	to	the	source	data.
You	use	Power	Query	to	import	two	tables	named	Order	Header	and	Order	Details	from	an	Azure	SQL	database.
The	Order	Header	table	relates	to	the	Order	Details	table	by	using	a	column	named	Order	ID	in	each	table.
You	need	to	combine	the	tables	into	a	single	query	that	contains	the	unique	columns	of	each	table.
What	should	you	select	in	Power	Query	Editor?
A.
Merge	queries

**Réponse exacte :**
A

**Explication courte :**
Correct	answer	is	A.	Merge	combines	columns.	Append	combines	rows.	The	question	is	about	related	tables.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column	and	set	the	data	type	of	the
new	column	to	Date.
B.
Change	the	data	type	of	the	Logged	column	to	Date.
C.
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.
Apply	the	Parse	function	from	the	Date	transformations	options	to	the	Logged	column.
Answer:	
C
Explanation:
Split	the	Logged	column	by	using	at	as	the	delimiter.

---

## Question 31
**Énoncé de la question :**
Correct	answer	is	A.	Merge	combines	columns.	Append	combines	rows.	The	question	is	about	related	tables.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column	and	set	the	data	type	of	the
new	column	to	Date.
B.
Change	the	data	type	of	the	Logged	column	to	Date.
C.
Split	the	Logged	column	by	using	at	as	the	delimiter.
D.
Apply	the	Parse	function	from	the	Date	transformations	options	to	the	Logged	column.
Answer:	
C
Explanation:
Split	the	Logged	column	by	using	at	as	the	delimiter.
HOTSPOT
-
You	have	a	folder	that	contains	50	JSON	files.
You	need	to	use	Power	BI	Desktop	to	make	the	metadata	of	the	files	available	as	a	single	dataset.	The	solution
must	NOT	store	the	data	of	the	JSON	files.
Which	type	of	data	source	should	you	use,	and	which	transformation	should	you	perform?	To	answer,	select	the
appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
Folder.
Delete	the	Content	column.
You	have	a	PBIX	file	that	imports	data	from	a	Microsoft	Excel	data	source	stored	in	a	file	share	on	a	local	network.
You	are	notified	that	the	Excel	data	source	was	moved	to	a	new	location.
You	need	to	update	the	PBIX	file	to	use	the	new	location.
What	are	three	ways	to	achieve	the	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

---

## Question 32
**Énoncé de la question :**
Folder.
Delete	the	Content	column.
You	have	a	PBIX	file	that	imports	data	from	a	Microsoft	Excel	data	source	stored	in	a	file	share	on	a	local	network.
You	are	notified	that	the	Excel	data	source	was	moved	to	a	new	location.
You	need	to	update	the	PBIX	file	to	use	the	new	location.
What	are	three	ways	to	achieve	the	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**
BDE

**Explication courte :**
B.From	the	Data	source	settings	in	Power	BI	Desktop,	configure	the	file	path.
D.From	Power	Query	Editor,	use	the	formula	bar	to	configure	the	file	path	for	the	applied	step.
E.From	Advanced	Editor	in	Power	Query	Editor,	configure	the	file	path	in	the	M	code.

---

## Question 34
**Énoncé de la question :**
B.From	the	Data	source	settings	in	Power	BI	Desktop,	configure	the	file	path.
D.From	Power	Query	Editor,	use	the	formula	bar	to	configure	the	file	path	for	the	applied	step.
E.From	Advanced	Editor	in	Power	Query	Editor,	configure	the	file	path	in	the	M	code.
HOTSPOT
-
You	have	a	Power	BI	semantic	model	that	contains	the	data	sources	shown	in	the	following	table.
You	need	to	configure	the	privacy	level	s	of	the	data	sources.
What	should	you	configure	for	each	data	source?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	answer	is	worth	one	point.

**Réponse exacte :**
B

**Explication courte :**
Correct	answer	is	B:Azure	DevOps	(Boards	only).

---

## Question 35
**Énoncé de la question :**
Correct	answer	is	B:Azure	DevOps	(Boards	only).
HOTSPOT
-
You	use	Power	Query	Editor	to	preview	the	data	shown	in	the	following	exhibit.
You	confirm	that	the	data	will	always	start	on	row	3,	and	row	3	will	always	contain	the	column	names.
How	should	you	shape	the	query?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	data	source	that	contains	a	column.	The	column	contains	case	sensitive	data.
You	have	a	Power	BI	semantic	model	in	DirectQuery	mode.
You	connect	to	the	model	and	discover	that	it	contains	undefined	values	and	errors.
You	need	to	resolve	the	issue.
Solution:	You	implicitly	convert	the	values	into	the	required	type.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
B

**Explication courte :**
Correct	answer	is	B:No.

---

## Question 36
**Énoncé de la question :**
Correct	answer	is	B:No.

**Réponse exacte :**
B

**Explication courte :**
No	is	a	right	answer.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	data	source	that	contains	a	column.	The	column	contains	case	sensitive	data.
You	have	a	Power	BI	semantic	model	in	DirectQuery	mode.
You	connect	to	the	model	and	discover	that	it	contains	undefined	values	and	errors.
You	need	to	resolve	the	issue.
Solution:	You	normalize	casing	in	the	source	query	or	Power	Query	Editor.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
A
Explanation:

---

## Question 38
**Énoncé de la question :**
No	is	a	right	answer.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	data	source	that	contains	a	column.	The	column	contains	case	sensitive	data.
You	have	a	Power	BI	semantic	model	in	DirectQuery	mode.
You	connect	to	the	model	and	discover	that	it	contains	undefined	values	and	errors.
You	need	to	resolve	the	issue.
Solution:	You	normalize	casing	in	the	source	query	or	Power	Query	Editor.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
A
Explanation:

**Réponse exacte :**
A

**Explication courte :**
Correct	answer	is	A:Yes.
You	have	a	Microsoft	Excel	file	in	a	Microsoft	OneDrive	folder.
The	file	must	be	imported	to	a	Power	BI	semantic	model.
You	need	to	ensure	that	the	semantic	model	can	be	refreshed	in	PowerBi.com.
Which	two	connectors	can	you	use	to	connect	to	the	file?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
Web
B.
Excel	Workbook
C.
Folder
D.
Text/CSV
E.
SharePoint	folder
Answer:	
AE
Explanation:
A.Web.

---

## Question 40
**Énoncé de la question :**
Correct	answer	is	A:Yes.
You	have	a	Microsoft	Excel	file	in	a	Microsoft	OneDrive	folder.
The	file	must	be	imported	to	a	Power	BI	semantic	model.
You	need	to	ensure	that	the	semantic	model	can	be	refreshed	in	PowerBi.com.
Which	two	connectors	can	you	use	to	connect	to	the	file?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
Web
B.
Excel	Workbook
C.
Folder
D.
Text/CSV
E.
SharePoint	folder
Answer:	
AE
Explanation:
A.Web.

**Réponse exacte :**
D

**Explication courte :**
Transform	the	column	to	contain	only	the	year.

---

## Question 42
**Énoncé de la question :**
Transform	the	column	to	contain	only	the	year.

**Réponse exacte :**
You	are	creating	a	report	in	Power	BI	Desktop.
You	load	a	data	extract	that	includes	a	free	text	field	named	coll.
You	need	to	analyze	the	frequency	distribution	of	the	string	lengths	in	col1.	The	solution	must	not	affect	the	size	of
the	model.
What	should	you	do?
A.	
In	the	report,	add	a	DAX	calculated	column	that	calculates	the	length	of	col1
B.	
In	the	report,	add	a	DAX	function	that	calculates	the	average	length	of	col1
C.	
From	Power	Query	Editor,	add	a	column	that	calculates	the	length	of	col1
D.	
From	Power	Query	Editor,	change	the	distribution	for	the	Column	profile	to	group	by	length	for	col1
Answer:	
D

**Explication courte :**
A	will	affect	the	size	of	the	model	as	would	C.
B	doesn't	give	you	enough	information	about	the	distribution	(just	the	average)
D	is	the	right	answer.
​
1.	Power	Query	Editor	->	View	->	Enable	Column	Profile
2.	Select	three	dots	(top	left	corner)	in	the	profile	pane	appear	at	the	bottom	of	the	Query	Editor	window.
3.	Group	By	->	Text	length

---

## Question 43
**Énoncé de la question :**
A	will	affect	the	size	of	the	model	as	would	C.
B	doesn't	give	you	enough	information	about	the	distribution	(just	the	average)
D	is	the	right	answer.
​
1.	Power	Query	Editor	->	View	->	Enable	Column	Profile
2.	Select	three	dots	(top	left	corner)	in	the	profile	pane	appear	at	the	bottom	of	the	Query	Editor	window.
3.	Group	By	->	Text	length

**Réponse exacte :**
A

**Explication courte :**
correct	ans	looks	as	A	since	an	app	would	prevent	to	change	the	layout
In	the	Power	BI	service,	members	of	a	workspace	have	access	to	datasets	in	the	workspace.	RLS	doesn't
restrict	this	data	access.	and	RLS	is	used	to	restrict	access	to	data	not	to	layout	of	the	report.	Members	are
allowed	to	change	the	report	layout.
Reference:
https://kunaltripathy.com/2021/10/06/bring-your-power-bi-to-power-apps-portal-part-ii/
You	need	to	provide	a	user	with	the	ability	to	add	members	to	a	workspace.	The	solution	must	use	the	principle	of
least	privilege.
Which	role	should	you	assign	to	the	user?
A.	
Viewer
B.	
Admin
C.	
Contributor
D.	
Member
Answer:	
D
Explanation:
Member	role	allows	adding	members	or	other	with	lower	permissions	to	the	workspace.

---

## Question 45
**Énoncé de la question :**
You	need	to	provide	a	user	with	the	ability	to	add	members	to	a	workspace.	The	solution	must	use	the	principle	of
least	privilege.
Which	role	should	you	assign	to	the	user?
A.	
Viewer
B.	
Admin
C.	
Contributor
D.	
Member
Answer:	
D
Explanation:
Member	role	allows	adding	members	or	other	with	lower	permissions	to	the	workspace.

**Réponse exacte :**
AD

**Explication courte :**
A:	Removing	uninteresting	rows	will	increase	query	performance.
D:	Splitting	the	Sales_Date	column	will	make	comparisons	on	the	Sales	date	faster.
The	Power	BI	Desktop	data	model	only	supports	date/time,	but	they	can	be	formatted	as	dates	or	times
independently.	Date/Time	–	Represents	both	a	date	and	time	value.	Underneath	the	covers,	the	Date/Time
value	is	stored	as	a	Decimal	Number	Type.	Since	there's	a	T	in	the	dates	column	before	split,	it's	saved	as	a
source	text	value.	Splitting	converts	it	to	a	numeric	value.	This	reduces	the	size.
You	build	a	report	to	analyze	customer	transactions	from	a	database	that	contains	the	tables	shown	in	the
following	table.

---

## Question 47
**Énoncé de la question :**
A:	Removing	uninteresting	rows	will	increase	query	performance.
D:	Splitting	the	Sales_Date	column	will	make	comparisons	on	the	Sales	date	faster.
The	Power	BI	Desktop	data	model	only	supports	date/time,	but	they	can	be	formatted	as	dates	or	times
independently.	Date/Time	–	Represents	both	a	date	and	time	value.	Underneath	the	covers,	the	Date/Time
value	is	stored	as	a	Decimal	Number	Type.	Since	there's	a	T	in	the	dates	column	before	split,	it's	saved	as	a
source	text	value.	Splitting	converts	it	to	a	numeric	value.	This	reduces	the	size.
You	build	a	report	to	analyze	customer	transactions	from	a	database	that	contains	the	tables	shown	in	the
following	table.

**Réponse exacte :**
D

**Explication courte :**
One	on	the	primary	Key	side	(customer	table),	many	on	the	foreign	key	side	(Transaction	table)	of	the	relation.
You	have	a	custom	connector	that	returns	ID,	From,	To,	Subject,	Body,	and	Has	Attachments	for	every	email	sent
during	the	past	year.	More	than	10	million	records	are	returned.
You	build	a	report	analyzing	the	internal	networks	of	employees	based	on	whom	they	send	emails	to.
You	need	to	prevent	report	recipients	from	reading	the	analyzed	emails.	The	solution	must	minimize	the	model	size.
What	should	you	do?
A.	
From	Model	view,	set	the	Subject	and	Body	columns	to	Hidden.
B.	
Remove	the	Subject	and	Body	columns	during	the	import.
C.	
Implement	row-level	security	(RLS)	so	that	the	report	recipients	can	only	see	results	based	on	the	emails
they	sent.
Answer:	
B
Explanation:
"prevent	report	recipients	from	reading	the	analyzed	emails"
The	Subject	and	the	Body	are	not	needed	in	the	report.	Dropping	them	resolves	the	security	problem	and
minimizes	the	model.

---

## Question 49
**Énoncé de la question :**
One	on	the	primary	Key	side	(customer	table),	many	on	the	foreign	key	side	(Transaction	table)	of	the	relation.
You	have	a	custom	connector	that	returns	ID,	From,	To,	Subject,	Body,	and	Has	Attachments	for	every	email	sent
during	the	past	year.	More	than	10	million	records	are	returned.
You	build	a	report	analyzing	the	internal	networks	of	employees	based	on	whom	they	send	emails	to.
You	need	to	prevent	report	recipients	from	reading	the	analyzed	emails.	The	solution	must	minimize	the	model	size.
What	should	you	do?
A.	
From	Model	view,	set	the	Subject	and	Body	columns	to	Hidden.
B.	
Remove	the	Subject	and	Body	columns	during	the	import.
C.	
Implement	row-level	security	(RLS)	so	that	the	report	recipients	can	only	see	results	based	on	the	emails
they	sent.
Answer:	
B
Explanation:
"prevent	report	recipients	from	reading	the	analyzed	emails"
The	Subject	and	the	Body	are	not	needed	in	the	report.	Dropping	them	resolves	the	security	problem	and
minimizes	the	model.

**Réponse exacte :**


**Explication courte :**
Box	1:
Row	label:	Name
See:	https://www.myonlinetraininghub.com/power-bi-organizational-data-types-in-
excel#:~:text=Power%20BI%20Organizational%20Data%20Types%20in%20Excel%20allow%20you%20to,company%2C%20to%20name%20a%20few.
Box	2:	ID	-
The	Key	column	field	value	provides	the	unique	ID	for	the	row.	This	value	enables	Excel	to	link	a	cell	to	a
specific	row	in	the	table.
Box	3:	Yes	-
In	the	Data	Types	Gallery	in	Excel,	your	users	can	find	data	from	featured	tables	in	your	Power	BI	datasets.
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-excel-featured-tables
You	have	the	Power	BI	model	shown	in	the	following	exhibit.
A	manager	can	represent	only	a	single	country.
You	need	to	use	row-level	security	(RLS)	to	meet	the	following	requirements:
✑
	The	managers	must	only	see	the	data	of	their	respective	country.
✑
	The	number	of	RLS	roles	must	be	minimized.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Create	a	single	role	that	filters	Country[Manager_Email]	by	using	the	USERNAME	DAX	function.
B.	
Create	a	single	role	that	filters	Country[Manager_Email]	by	using	the	USEROBJECTID	DAX	function.
C.	
For	the	relationship	between	Purchase	Detail	and	Purchase,	select	Apply	security	filter	in	both	directions.
D.	
Create	one	role	for	each	country.
E.	
For	the	relationship	between	Purchase	and	Purchase	Detail,	change	the	Cross	filter	direction	to	Single.
Answer:	
AC
Explanation:
A:	You	can	take	advantage	of	the	DAX	functions	username()	or	userprincipalname()	within	your	dataset.	You
can	use	them	within	expressions	in	Power	BI
Desktop.	When	you	publish	your	model,	it	will	be	used	within	the	Power	BI	service.
Note:	To	define	security	roles,	follow	these	steps.
Import	data	into	your	Power	BI	Desktop	report,	or	configure	a	DirectQuery	connection.
1.	From	the	Modeling	tab,	select	Manage	Roles.
2.	From	the	Manage	roles	window,	select	Create.
3.	Under	Roles,	provide	a	name	for	the	role.
4.	Under	Tables,	select	the	table	to	which	you	want	to	apply	a	DAX	rule.

---

## Question 51
**Énoncé de la question :**
excel#:~:text=Power%20BI%20Organizational%20Data%20Types%20in%20Excel%20allow%20you%20to,company%2C%20to%20name%20a%20few.
Box	2:	ID	-
The	Key	column	field	value	provides	the	unique	ID	for	the	row.	This	value	enables	Excel	to	link	a	cell	to	a
specific	row	in	the	table.
Box	3:	Yes	-
In	the	Data	Types	Gallery	in	Excel,	your	users	can	find	data	from	featured	tables	in	your	Power	BI	datasets.
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-excel-featured-tables
You	have	the	Power	BI	model	shown	in	the	following	exhibit.
A	manager	can	represent	only	a	single	country.
You	need	to	use	row-level	security	(RLS)	to	meet	the	following	requirements:
✑
	The	managers	must	only	see	the	data	of	their	respective	country.
✑
	The	number	of	RLS	roles	must	be	minimized.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Create	a	single	role	that	filters	Country[Manager_Email]	by	using	the	USERNAME	DAX	function.
B.	
Create	a	single	role	that	filters	Country[Manager_Email]	by	using	the	USEROBJECTID	DAX	function.
C.	
For	the	relationship	between	Purchase	Detail	and	Purchase,	select	Apply	security	filter	in	both	directions.
D.	
Create	one	role	for	each	country.
E.	
For	the	relationship	between	Purchase	and	Purchase	Detail,	change	the	Cross	filter	direction	to	Single.
Answer:	
AC
Explanation:
A:	You	can	take	advantage	of	the	DAX	functions	username()	or	userprincipalname()	within	your	dataset.	You
can	use	them	within	expressions	in	Power	BI
Desktop.	When	you	publish	your	model,	it	will	be	used	within	the	Power	BI	service.
Note:	To	define	security	roles,	follow	these	steps.
Import	data	into	your	Power	BI	Desktop	report,	or	configure	a	DirectQuery	connection.
1.	From	the	Modeling	tab,	select	Manage	Roles.
2.	From	the	Manage	roles	window,	select	Create.
3.	Under	Roles,	provide	a	name	for	the	role.
4.	Under	Tables,	select	the	table	to	which	you	want	to	apply	a	DAX	rule.

**Réponse exacte :**


**Explication courte :**
Box	1:	cross	filter	direction	-
As	the	answer	correctly	states	"Assume	Referential	Integrity"	only	works	for	direct	query	connections.
Box	2:	Star	schema	-
Star	schema	is	a	mature	modeling	approach	widely	adopted	by	relational	data	warehouses.	It	requires
modelers	to	classify	their	model	tables	as	either	dimension	or	fact.
Generally,	dimension	tables	contain	a	relatively	small	number	of	rows.	Fact	tables,	on	the	other	hand,	can
contain	a	very	large	number	of	rows	and	continue	to	grow	over	time.
Example:
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-assume-referential-integrity
https://docs.microsoft.com/en-us/power-bi/guidance/star-schema

---

## Question 52
**Énoncé de la question :**
https://docs.microsoft.com/en-us/power-bi/guidance/star-schema
HOTSPOT	-
You	have	a	Power	BI	model	that	contains	a	table	named	Sales	and	a	related	date	table.	Sales	contains	a	measure
named	Total	Sales.
You	need	to	create	a	measure	that	calculates	the	total	sales	from	the	equivalent	month	of	the	previous	year.
How	should	you	complete	the	calculation?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
CALCULATE
SAMEPERIODLASTYEAR
'DATE'[DATE]
Box	1:	CALCULATE	-
Box	2:	SAMEPERIODLASTYEAR
accepts	a	data	column,	Month	will	usually	be	either	text	(Jan)	or	Integer	(1).	so:	CALCULATE([Total	Sales],
SAMEPERIODLASTYEAR('Date'[Date]))
Box	3:	'DATE'	[DATE]
Reference:
https://docs.microsoft.com/en-us/dax/parallelperiod-function-dax	https://docs.microsoft.com/en-
us/dax/sameperiodlastyear-function-dax
DRAG	DROP	-
You	plan	to	create	a	report	that	will	display	sales	data	from	the	last	year	for	multiple	regions.
You	need	to	restrict	access	to	individual	rows	of	the	data	on	a	per	region-basis	by	using	roles.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
With	respect,	you	can	not	assign	users	to	a	role	until	AFTER	the	report	has	been	published	to	the	Power	BI
Service.	Those	posting	that	you	create	the	role	and	then	assign	users	to	the	role	BEFORE	publishing	are
incorrect.	Roles	are	created	in	Power	BI	Desktop.	Desktop	does	not	have	any	way	to	assign	users	to	the	roles.
They	are	empty	when	created.	Role	assignment	happens	in	the	service.
Publish	the	report	to	the	Power	BI	service.	Go	to	your	Workspace,	using	the	Dataset,	select	the	More	Options
menu(...)	and	click	Security.	This	is	where	the	Roles	are	populated.
1)	Import	your	data	into	Power	BI	Desktop
2)	Create	the	role	definition	(on	the	Modeling	tab)
3)	Publish	the	report	to	the	Power	BI	service
4)	Assign	users	to	the	role

---

## Question 53
**Énoncé de la question :**
https://docs.microsoft.com/en-
us/dax/sameperiodlastyear-function-dax
DRAG	DROP	-
You	plan	to	create	a	report	that	will	display	sales	data	from	the	last	year	for	multiple	regions.
You	need	to	restrict	access	to	individual	rows	of	the	data	on	a	per	region-basis	by	using	roles.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
With	respect,	you	can	not	assign	users	to	a	role	until	AFTER	the	report	has	been	published	to	the	Power	BI
Service.	Those	posting	that	you	create	the	role	and	then	assign	users	to	the	role	BEFORE	publishing	are
incorrect.	Roles	are	created	in	Power	BI	Desktop.	Desktop	does	not	have	any	way	to	assign	users	to	the	roles.
They	are	empty	when	created.	Role	assignment	happens	in	the	service.
Publish	the	report	to	the	Power	BI	service.	Go	to	your	Workspace,	using	the	Dataset,	select	the	More	Options
menu(...)	and	click	Security.	This	is	where	the	Roles	are	populated.
1)	Import	your	data	into	Power	BI	Desktop
2)	Create	the	role	definition	(on	the	Modeling	tab)
3)	Publish	the	report	to	the	Power	BI	service
4)	Assign	users	to	the	role

**Réponse exacte :**


**Explication courte :**
1.Merge	[Region_Manager]	and	[Manager]	by	using	an	inner	join.
3.Merge	[Sales_Region]	and	[Sales_Manager]	by	using	an	inner	join.
6.Merge	[Sales_Region]	and	[Region_Manager]	by	using	an	inner	join.

---

## Question 54
**Énoncé de la question :**
1.Merge	[Region_Manager]	and	[Manager]	by	using	an	inner	join.
3.Merge	[Sales_Region]	and	[Sales_Manager]	by	using	an	inner	join.
6.Merge	[Sales_Region]	and	[Region_Manager]	by	using	an	inner	join.

**Réponse exacte :**
D

**Explication courte :**
One	page	with	many	visuals	may	also	make	your	report	loading	slow.	Please	appropriately	reduce	the	number
of	visualizations	on	one	page.
Reference:
https://community.powerbi.com/t5/Desktop/Visuals-are-loading-extremely-slow/td-p/1565668

---

## Question 56
**Énoncé de la question :**
HOTSPOT	-
You	are	creating	a	Microsoft	Power	BI	imported	data	model	to	perform	basket	analysis.	The	goal	of	the	analysis	is
to	identify	which	products	are	usually	bought	together	in	the	same	transaction	across	and	within	sales	territories.
You	import	a	fact	table	named	Sales	as	shown	in	the	exhibit.	(Click	the	Exhibit	tab.)
The	related	dimension	tables	are	imported	into	the	model.
Sales	contains	the	data	shown	in	the	following	table.

**Réponse exacte :**


**Explication courte :**
Box	1:	Yes	-
Those	two	columns	not	need	in	the	analysis.
Box	2:	No	-
Can	remove	the	surrogate	key	OrderDateKey	from	the	analysis.
Box	3:	No	-
Tax	charged	not	relevant	for	the	analysis.
You	have	a	Microsoft	Power	BI	data	model	that	contains	three	tables	named	Orders,	Date,	and	City.	There	is	a	one-
to-many	relationship	between	Date	and
Orders	and	between	City	and	Orders.
The	model	contains	two	row-level	security	(RLS)	roles	named	Role1	and	Role2.	Role1	contains	the	following	filter.
City[State	Province]	=	"Kentucky"
Role2	contains	the	following	filter.
Date[Calendar	Year]	=	2020	-
If	a	user	is	a	member	of	both	Role1	and	Role2,	what	data	will	they	see	in	a	report	that	uses	the	model?
A.	
The	user	will	see	data	for	which	the	State	Province	value	is	Kentucky	or	where	the	Calendar	Year	is	2020.
B.	
The	user	will	receive	an	error	and	will	not	be	able	to	see	the	data	in	the	report.
C.	
The	user	will	only	see	data	for	which	the	State	Province	value	is	Kentucky.
D.	
The	user	will	only	see	data	for	which	the	State	Province	value	is	Kentucky	and	the	Calendar	Year	is	2020.
Answer:	
A
Explanation:
A,	from	the	Microsoft	documentation	(https://docs.microsoft.com/en-us/power-bi/guidance/rls-guidance):
"When	a	report	user	is	assigned	to	multiple	roles,	RLS	filters	become	additive.	It	means	report	users	can	see
table	rows	that	represent	the	union	of	those	filters."
This	means	that	you	would	see	all	data	where	either	Role1	OR	Role2	applies,	so	the	answer	is	A	not	D.
Example	from	MS	Learn	linked	below:
https://learn.microsoft.com/en-us/power-bi/guidance/rls-guidance
"Consider	a	model	with	two	roles:	The	first	role,	named	Workers,	restricts	access	to	all	Payroll	table	rows	by
using	the	following	rule	expression:
DAX:
FALSE()
A	rule	will	return	no	table	rows	when	its	expression	evaluates	to	false.
Yet,	a	second	role,	named	Managers,	allows	access	to	all	Payroll	table	rows	by	using	the	following	rule
expression:
DAX:
TRUE()

---

## Question 57
**Énoncé de la question :**
"When	a	report	user	is	assigned	to	multiple	roles,	RLS	filters	become	additive.	It	means	report	users	can	see
table	rows	that	represent	the	union	of	those	filters."
This	means	that	you	would	see	all	data	where	either	Role1	OR	Role2	applies,	so	the	answer	is	A	not	D.
Example	from	MS	Learn	linked	below:
https://learn.microsoft.com/en-us/power-bi/guidance/rls-guidance
"Consider	a	model	with	two	roles:	The	first	role,	named	Workers,	restricts	access	to	all	Payroll	table	rows	by
using	the	following	rule	expression:
DAX:
FALSE()
A	rule	will	return	no	table	rows	when	its	expression	evaluates	to	false.
Yet,	a	second	role,	named	Managers,	allows	access	to	all	Payroll	table	rows	by	using	the	following	rule
expression:
DAX:
TRUE()

**Réponse exacte :**
B

**Explication courte :**
This	would	load	the	entire	table	in	the	first	step.
Instead:	You	add	a	WHERE	clause	to	the	SQL	statement.
Reference:
https://docs.microsoft.com/en-us/power-query/native-database-query
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	are	modeling	data	by	using	Microsoft	Power	BI.	Part	of	the	data	model	is	a	large	Microsoft	SQL	Server	table
named	Order	that	has	more	than	100	million	records.
During	the	development	process,	you	need	to	import	a	sample	of	the	data	from	the	Order	table.
Solution:	You	write	a	DAX	expression	that	uses	the	FILTER	function.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Instead:	You	add	a	WHERE	clause	to	the	SQL	statement.
Note:	DAX	is	not	a	language	designed	to	fetch	the	data	like	SQL	rather	than	used	for	data	analysis	purposes.
It	is	always	a	better	and	recommended	approach	to	transform	the	data	as	close	to	the	data	source	itself.	For
example,	your	data	source	is	a	relational	database;	then,	it's	better	to	go	with	T-SQL.

---

## Question 59
**Énoncé de la question :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	are	modeling	data	by	using	Microsoft	Power	BI.	Part	of	the	data	model	is	a	large	Microsoft	SQL	Server	table
named	Order	that	has	more	than	100	million	records.
During	the	development	process,	you	need	to	import	a	sample	of	the	data	from	the	Order	table.
Solution:	You	write	a	DAX	expression	that	uses	the	FILTER	function.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Instead:	You	add	a	WHERE	clause	to	the	SQL	statement.
Note:	DAX	is	not	a	language	designed	to	fetch	the	data	like	SQL	rather	than	used	for	data	analysis	purposes.
It	is	always	a	better	and	recommended	approach	to	transform	the	data	as	close	to	the	data	source	itself.	For
example,	your	data	source	is	a	relational	database;	then,	it's	better	to	go	with	T-SQL.

**Réponse exacte :**
A

**Explication courte :**
Power	Query	enables	you	to	specify	your	native	database	query	in	a	text	box	under	Advanced	options	when
connecting	to	a	database.	In	the	example	below,	you'll	import	data	from	a	SQL	Server	database	using	a	native
database	query	entered	in	the	SQL	statement	text	box.
1.	Connect	to	a	SQL	Server	database	using	Power	Query.	Select	the	SQL	Server	database	option	in	the
connector	selection.
2.	In	the	SQL	Server	database	popup	window:
3.	Specify	the	Server	and	Database	where	you	want	to	import	data	from	using	native	database	query.
4.	Under	Advanced	options,	select	the	SQL	statement	field	and	paste	or	enter	your	native	database	query,
then	select	OK.

---

## Question 61
**Énoncé de la question :**
Power	Query	enables	you	to	specify	your	native	database	query	in	a	text	box	under	Advanced	options	when
connecting	to	a	database.	In	the	example	below,	you'll	import	data	from	a	SQL	Server	database	using	a	native
database	query	entered	in	the	SQL	statement	text	box.
1.	Connect	to	a	SQL	Server	database	using	Power	Query.	Select	the	SQL	Server	database	option	in	the
connector	selection.
2.	In	the	SQL	Server	database	popup	window:
3.	Specify	the	Server	and	Database	where	you	want	to	import	data	from	using	native	database	query.
4.	Under	Advanced	options,	select	the	SQL	statement	field	and	paste	or	enter	your	native	database	query,
then	select	OK.

**Réponse exacte :**


**Explication courte :**
1.	Use	first	row	as	header
2.	Unpivot	all	columns	other	than	"Measure"
3.	Rename	"Attribute"	to	"Year"
4.	Change	data	type	of	"Year"	column	to	Date
Reference:
https://docs.microsoft.com/en-us/power-query/unpivot-column

---

## Question 62
**Énoncé de la question :**
HOTSPOT	-
You	are	creating	an	analytics	report	that	will	consume	data	from	the	tables	shown	in	the	following	table.

**Réponse exacte :**


**Explication courte :**
Box	1:	Hide	-
Need	in	the	relation,	so	cannot	delete	it.
Box	2:	Delete	-
Reference:
https://community.powerbi.com/t5/Desktop/How-to-Hide-a-Column-in-power-Bi/m-p/414470

---

## Question 63
**Énoncé de la question :**
HOTSPOT	-
You	plan	to	create	Power	BI	dataset	to	analyze	attendance	at	a	school.	Data	will	come	from	two	separate	views
named	View1	and	View2	in	an	Azure	SQL	database.
View1	contains	the	columns	shown	in	the	following	table.
View2	contains	the	columns	shown	in	the	following	table.

**Réponse exacte :**


**Explication courte :**
Box	1:	Teacher	Dimension-
Box	2:	Class	Dimension-
teacher's	dim	and	class	dim	because	teacher	name	and	period	number	are	static	information	that	are	directly
related	to	the	keys	(teacher	ID	and	class	ID)	so	they	belong	in	the	relevant	dimension	tables.	Since	the	"Class
ID	is	unique	for	the	class,	period,	teacher	and	school	year"	this	information	should	be	included	in	the	class
dimension	table	and	not	repeated	for	each	student's	attendance	to	keep	your	model	as	small	as	possible	and
to	avoid	mistakes.
Reference:
https://docs.microsoft.com/en-us/power-bi/guidance/star-schema
You	have	the	Power	BI	model	shown	in	the	following	exhibit.
There	are	four	departments	in	the	Departments	table.
You	need	to	ensure	that	users	can	see	the	data	of	their	respective	department	only.
What	should	you	do?
A.	
Create	a	slicer	that	filters	Departments	based	on	DepartmentID.
B.	
Create	a	row-level	security	(RLS)	role	for	each	department,	and	then	define	the	membership	of	the	role.
C.	
Create	a	DepartmentID	parameter	to	filter	the	Departments	table.
D.	
To	the	ConfidentialData	table,	add	a	calculated	measure	that	uses	the	CURRENTGROUP	DAX	function.
Answer:	
B
Explanation:
Row-level	security	(RLS)	with	Power	BI	can	be	used	to	restrict	data	access	for	given	users.	Filters	restrict	data
access	at	the	row	level,	and	you	can	define	filters	within	roles.

---

## Question 64
**Énoncé de la question :**
You	have	the	Power	BI	model	shown	in	the	following	exhibit.
There	are	four	departments	in	the	Departments	table.
You	need	to	ensure	that	users	can	see	the	data	of	their	respective	department	only.
What	should	you	do?
A.	
Create	a	slicer	that	filters	Departments	based	on	DepartmentID.
B.	
Create	a	row-level	security	(RLS)	role	for	each	department,	and	then	define	the	membership	of	the	role.
C.	
Create	a	DepartmentID	parameter	to	filter	the	Departments	table.
D.	
To	the	ConfidentialData	table,	add	a	calculated	measure	that	uses	the	CURRENTGROUP	DAX	function.
Answer:	
B
Explanation:
Row-level	security	(RLS)	with	Power	BI	can	be	used	to	restrict	data	access	for	given	users.	Filters	restrict	data
access	at	the	row	level,	and	you	can	define	filters	within	roles.

**Réponse exacte :**
B

**Explication courte :**
By	default,	row-level	security	filtering	uses	single-directional	filters,	whether	the	relationships	are	set	to
single	direction	or	bi-directional.	You	can	manually	enable	bi-directional	cross-filtering	with	row-level	security
by	selecting	the	relationship	and	checking	the	Apply	security	filter	in	both	directions	checkbox.	Select	this
option	when	you've	also	implemented	dynamic	row-level	security	at	the	server	level,	where	row-level	security
is	based	on	username	or	login	ID.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls

---

## Question 66
**Énoncé de la question :**
HOTSPOT	-
You	have	a	column	named	UnitsInStock	as	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Box	1:	75	rows	-
Is	nullable	allows	NULL	values	in	the	column.
Box	2:	reduce	-
We're	not	dealing	with	a	matric	here,	we're	dealing	with	a	simple	table.	In	simple	tables	values	that	occur
more	than	once	won't	be	shown	in	the	rows	multiple	times.	Since	you're	they	tell	you	you	have	51	unique
values	(and	the	other	ones	aren't	null	values)	you	can	be	sure	it's	more	than	51.	Since	you'll	already	have	51
rows	of	unique	values.
So	the	first	is	answer	is	75.
Furthermore,	when	you	add	another	table,	change	the	sign	to	summarize,	you	will	add	up	all	the	values	of	the
51	unique	values	and	all	the	rest.	Which	means	you	will	get	one	single	row,	displaying	the	sum	of	all	these
values.
Therefore,	the	second	answer	is	reduce.
Reference:
https://blog.crossjoin.co.uk/2019/01/20/is-nullable-column-property-power-bi/

---

## Question 67
**Énoncé de la question :**
HOTSPOT	-
You	have	a	Power	BI	report.
You	have	the	following	tables.
You	have	the	following	DAX	measure.
Accounts	:=
CALCULATE	(
DISTINCTCOUNT	(Balances[AccountID]),
LASTDATE	('Date'[Date])
For	each	of	the	following	statements,	select	Yes	if	the	statement	is	true.	Otherwise,	select	No.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:
Explanation:
Box	1:	No	-
It	will	show	the	total	number	of	accounts	that	were	live	at	the	last	day	of	the	year	only.
Note:
DISTINCTCOUNT	counts	the	number	of	distinct	values	in	a	column.
LASTDATE	returns	the	last	date	in	the	current	context	for	the	specified	column	of	dates.

**Réponse exacte :**
AB

**Explication courte :**
Incorrect:
Not	C:	A	calculated	table	would	increase	the	data	model	size.
Not	D:	Need	Impression_date	etc.

---

## Question 70
**Énoncé de la question :**
Incorrect:
Not	C:	A	calculated	table	would	increase	the	data	model	size.
Not	D:	Need	Impression_date	etc.

**Réponse exacte :**
D

**Explication courte :**
The	DateKey	and	MovementDate	columns	have	the	same	information.	Movementdate	can	be	removed.
D,	because	the	best	way	to	reduce	the	data	model	size	is	to	remove	the	unnecessary	column.
Incorrect:
Not	C:	Integer	data	type	would	lose	data.

---

## Question 71
**Énoncé de la question :**
The	DateKey	and	MovementDate	columns	have	the	same	information.	Movementdate	can	be	removed.
D,	because	the	best	way	to	reduce	the	data	model	size	is	to	remove	the	unnecessary	column.
Incorrect:
Not	C:	Integer	data	type	would	lose	data.
HOTSPOT	-
You	are	enhancing	a	Power	BI	model	that	has	DAX	calculations.
You	need	to	create	a	measure	that	returns	the	year-to-date	total	sales	from	the	same	date	of	the	previous
calendar	year.
Which	DAX	functions	should	you	use?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:	CALCULATE	-
Example:
Total	sales	on	the	last	selected	date	=
CALCULATE	(
SUM	(	Sales[Sales	Amount]	),
'Sales'[OrderDateKey]	=	MAX	(	'Sales'[OrderDateKey]	)
)
Box	2:	SUM	-
Box	3:	DatesBetween
This	is	due	to	the	expected	parameters.	DatesBetween	expects	two	parameters	as	per	the	exhibit,
SamePeriodLastYear	expects	one	parameter	(but	two	are	used	in	the	exhibit)
Reference:
https://docs.microsoft.com/en-us/dax/calculate-function-dax
https://dax.guide/sameperiodlastyear/
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	are	modeling	data	by	using	Microsoft	Power	BI.	Part	of	the	data	model	is	a	large	Microsoft	SQL	Server	table
named	Order	that	has	more	than	100	million	records.
During	the	development	process,	you	need	to	import	a	sample	of	the	data	from	the	Order	table.
Solution:	You	add	a	report-level	filter	that	filters	based	on	the	order	date.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
You	want	the	raw	data,	not	a	report	with	the	data.
Instead	add	a	WHERE	clause	to	the	SQL	statement.
Reference:
https://docs.microsoft.com/en-us/power-query/native-database-query
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
✑
	Due	Date
✑
	Order	Date
✑
	Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	the	date	foreign	keys.
Solution:	For	each	date	foreign	key,	you	add	inactive	relationships	between	the	sales	table	and	the	date	table.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Instead:	Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to
create	Order	Date	and	Delivery	Date	as	calculated	tables.

---

## Question 73
**Énoncé de la question :**
https://dax.guide/sameperiodlastyear/
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	are	modeling	data	by	using	Microsoft	Power	BI.	Part	of	the	data	model	is	a	large	Microsoft	SQL	Server	table
named	Order	that	has	more	than	100	million	records.
During	the	development	process,	you	need	to	import	a	sample	of	the	data	from	the	Order	table.
Solution:	You	add	a	report-level	filter	that	filters	based	on	the	order	date.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
You	want	the	raw	data,	not	a	report	with	the	data.
Instead	add	a	WHERE	clause	to	the	SQL	statement.
Reference:
https://docs.microsoft.com/en-us/power-query/native-database-query
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
✑
	Due	Date
✑
	Order	Date
✑
	Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	the	date	foreign	keys.
Solution:	For	each	date	foreign	key,	you	add	inactive	relationships	between	the	sales	table	and	the	date	table.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Instead:	Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to
create	Order	Date	and	Delivery	Date	as	calculated	tables.

**Réponse exacte :**
A

**Explication courte :**
1.	It's	not	going	to	be	great	solution	from	the	performance	side...but	that's	not	part	of	the	requirements
2.	Answer	is	YES.That's	not	the	best	solution	regarding	the	performance	but	it's	not	the	subject.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
✑
	Due	Date
✑
	Order	Date
✑
	Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	the	date	foreign	keys.
Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to	create	Order
Date	and	Delivery	Date	as	calculated	tables.
Does	this	meet	the	goal?

---

## Question 75
**Énoncé de la question :**
1.	It's	not	going	to	be	great	solution	from	the	performance	side...but	that's	not	part	of	the	requirements
2.	Answer	is	YES.That's	not	the	best	solution	regarding	the	performance	but	it's	not	the	subject.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
✑
	Due	Date
✑
	Order	Date
✑
	Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	the	date	foreign	keys.
Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to	create	Order
Date	and	Delivery	Date	as	calculated	tables.
Does	this	meet	the	goal?

**Réponse exacte :**
A

**Explication courte :**
Refactoring	methodology	-
Here's	a	methodology	to	refactor	a	model	from	a	single	role-playing	dimension-type	table,	to	a	design	with
one	table	per	role.
1.	Remove	any	inactive	relationships.
2.	Consider	renaming	the	role-playing	dimension-type	table	to	better	describe	its	role.	In	the	example	(not
present	here),	the	Airport	table	is	related	to	the
ArrivalAirport	column	of	the	Flight	table,	so	it's	renamed	as	Arrival	Airport.
3.	Create	a	copy	of	the	role-playing	table,	providing	it	with	a	name	that	reflects	its	role.	If	it's	an	Import	table,
we	recommend	defining	a	calculated	table.	If	it's	a
DirectQuery	table,	you	can	duplicate	the	Power	Query	query.
In	the	example,	the	Departure	Airport	table	was	created	by	using	the	following	calculated	table	definition.
Departure	Airport	=	'Arrival	Airport'
Create	an	active	relationship	to	relate	the	new	table.
4.	Consider	renaming	the	columns	in	the	tables	so	they	accurately	reflect	their	role.	In	the	example,	all
columns	are	prefixed	with	the	word	Departure	or	Arrival.
These	names	ensure	report	visuals,	by	default,	will	have	self-describing	and	non-ambiguous	labels.	It	also
improves	the	Q&A	experience,	allowing	users	to	easily	write	their	questions.
5.	Consider	adding	descriptions	to	role-playing	tables.	(In	the	Fields	pane,	a	description	appears	in	a	tooltip
when	a	report	author	hovers	their	cursor	over	the	table.)	This	way,	you	can	communicate	any	additional	filter
propagation	details	to	your	report	authors.
Reference:
https://docs.microsoft.com/en-us/power-bi/guidance/relationships-active-inactive
DRAG	DROP	-
You	receive	revenue	data	that	must	be	included	in	Microsoft	Power	BI	reports.
You	preview	the	data	from	a	Microsoft	Excel	source	in	Power	Query	as	shown	in	the	following	exhibit.
You	plan	to	create	several	visuals	from	the	data,	including	a	visual	that	shows	revenue	split	by	year	and	product.
You	need	to	transform	the	data	to	ensure	that	you	can	build	the	visuals.	The	solution	must	ensure	that	the	columns
are	named	appropriately	for	the	data	that	they	contain.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:

---

## Question 76
**Énoncé de la question :**
DRAG	DROP	-
You	receive	revenue	data	that	must	be	included	in	Microsoft	Power	BI	reports.
You	preview	the	data	from	a	Microsoft	Excel	source	in	Power	Query	as	shown	in	the	following	exhibit.
You	plan	to	create	several	visuals	from	the	data,	including	a	visual	that	shows	revenue	split	by	year	and	product.
You	need	to	transform	the	data	to	ensure	that	you	can	build	the	visuals.	The	solution	must	ensure	that	the	columns
are	named	appropriately	for	the	data	that	they	contain.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:

**Réponse exacte :**


**Explication courte :**
Correct	Sequence	=	2>3>4
Select	Use	First	Row	as	Headers
Select	Department	and	Product	and	Unpivot	Other	Column
Rename	the	Attribute	column	to	YEAR	and	the	Value	column	to	REVENUE

---

## Question 77
**Énoncé de la question :**
Correct	Sequence	=	2>3>4
Select	Use	First	Row	as	Headers
Select	Department	and	Product	and	Unpivot	Other	Column
Rename	the	Attribute	column	to	YEAR	and	the	Value	column	to	REVENUE
HOTSPOT	-
You	have	a	Power	BI	report	named	Orders	that	supports	the	following	analysis:
✑
	Total	sales	over	time
✑
	The	count	of	orders	over	time
✑
	New	and	repeat	customer	counts
The	data	model	size	is	nearing	the	limit	for	a	dataset	in	shared	capacity.
The	model	view	for	the	dataset	is	shown	in	the	following	exhibit.
The	data	view	for	the	Orders	table	is	shown	in	the	following	exhibit.
The	Orders	table	relates	to	the	Customers	table	by	using	the	CustomerID	column.
The	Orders	table	relates	to	the	Date	table	by	using	the	OrderDate	column.
For	each	of	the	following	statements,	select	Yes	if	the	statement	is	true,	Otherwise,	select	No.

**Réponse exacte :**


**Explication courte :**
Box	1:	No	-
Would	not	support	total	sales	over	time.
Box	2:	No	-
Would	not	support	new	and	repeat	customer	counts
Box	3:	Yes

---

## Question 78
**Énoncé de la question :**
Box	1:	No	-
Would	not	support	total	sales	over	time.
Box	2:	No	-
Would	not	support	new	and	repeat	customer	counts
Box	3:	Yes
HOTSPOT	-
You	are	building	a	financial	report	by	using	Power	BI.
You	have	a	table	named	financials	that	contains	a	column	named	Date	and	a	column	named	Sales.
You	need	to	create	a	measure	that	calculates	the	relative	change	in	sales	as	compared	to	the	previous	quarter.
How	should	you	complete	the	measure?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:	CALCULATE	-
Calculate	the	sum.
Box	2:	DATEADD	-
DATEADD	-1	QUARTER	will	give	the	previous	month.
Box	3:	DIVIDE	-
Use	DIVIDE	to	get	the	relative	change.
DRAG	DROP	-
You	are	creating	a	Power	BI	model	and	report.
You	have	a	single	table	in	a	data	model	named	Product.	Product	contains	the	following	fields:
✑
	ID
✑
	Name
✑
	Color
✑
	Category

---

## Question 79
**Énoncé de la question :**
Box	1:	CALCULATE	-
Calculate	the	sum.
Box	2:	DATEADD	-
DATEADD	-1	QUARTER	will	give	the	previous	month.
Box	3:	DIVIDE	-
Use	DIVIDE	to	get	the	relative	change.
DRAG	DROP	-
You	are	creating	a	Power	BI	model	and	report.
You	have	a	single	table	in	a	data	model	named	Product.	Product	contains	the	following	fields:
✑
	ID
✑
	Name
✑
	Color
✑
	Category

**Réponse exacte :**


**Explication courte :**
Box	1:	TOPN	-
TOPN	returns	the	top	N	rows	of	the	specified	table.
Syntax:	TOPN(<n_value>,	<table>,	<orderBy_expression>,	[<order>[,	<orderBy_expression>,	[<order>]]
�
])
Box	2:	DESC	-
Descending	order	to	get	the	highest	values	first.
Reference:
https://docs.microsoft.com/en-us/dax/topn-function-dax
You	are	creating	a	sales	report	in	Power	BI	for	the	NorthWest	region	sales	territory	of	your	company.	Data	will
come	from	a	view	in	a	Microsoft	SQL	Server	database.	A	sample	of	the	data	is	shown	in	the	following	table:

---

## Question 80
**Énoncé de la question :**
You	are	creating	a	sales	report	in	Power	BI	for	the	NorthWest	region	sales	territory	of	your	company.	Data	will
come	from	a	view	in	a	Microsoft	SQL	Server	database.	A	sample	of	the	data	is	shown	in	the	following	table:

**Réponse exacte :**
CD

**Explication courte :**
C:	Remove	columns	that	are	not	used	in	the	report.
D:	Reduce	the	number	of	rows.
Incorrect:
Not	A:	Not	possible.
Not	B:	Need	CustomerKey	to	count	of	customers	who	placed	an	order
You	are	creating	a	Power	BI	model	that	contains	a	table	named	Store.	Store	contains	the	following	fields.
You	plan	to	create	a	map	visual	that	will	show	store	locations	and	provide	the	ability	to	drill	down	from	Country	to
State/Province	to	City.
What	should	you	do	to	ensure	that	the	locations	are	mapped	properly?
A.	
Change	the	data	type	of	City,	State/Province,	and	Country.
B.	
Set	Summarization	for	City,	State/Province,	and	Country	to	Don't	summarize.
C.	
Set	the	data	category	of	City,	State/Province,	and	Country.
D.	
Create	a	calculated	column	that	concatenates	the	values	in	City,	State/Province,	and	Country.
Answer:	
C
Explanation:
A	hierarchy	is	a	set	of	fields	categorized	in	a	hierarchical	way	that	one	level	is	the	parent	of	another	level.
Values	of	the	parent	level	can	be	drilled	down	to	the	lower	level.
Create	Hierarchy	-
Right-click	on	the	field	you	want	to	set	as	level	1	of	the	hierarchy	in	the	fields	list,	and	then	select	Create
Hierarchy.

---

## Question 82
**Énoncé de la question :**
C:	Remove	columns	that	are	not	used	in	the	report.
D:	Reduce	the	number	of	rows.
Incorrect:
Not	A:	Not	possible.
Not	B:	Need	CustomerKey	to	count	of	customers	who	placed	an	order
You	are	creating	a	Power	BI	model	that	contains	a	table	named	Store.	Store	contains	the	following	fields.
You	plan	to	create	a	map	visual	that	will	show	store	locations	and	provide	the	ability	to	drill	down	from	Country	to
State/Province	to	City.
What	should	you	do	to	ensure	that	the	locations	are	mapped	properly?
A.	
Change	the	data	type	of	City,	State/Province,	and	Country.
B.	
Set	Summarization	for	City,	State/Province,	and	Country	to	Don't	summarize.
C.	
Set	the	data	category	of	City,	State/Province,	and	Country.
D.	
Create	a	calculated	column	that	concatenates	the	values	in	City,	State/Province,	and	Country.
Answer:	
C
Explanation:
A	hierarchy	is	a	set	of	fields	categorized	in	a	hierarchical	way	that	one	level	is	the	parent	of	another	level.
Values	of	the	parent	level	can	be	drilled	down	to	the	lower	level.
Create	Hierarchy	-
Right-click	on	the	field	you	want	to	set	as	level	1	of	the	hierarchy	in	the	fields	list,	and	then	select	Create
Hierarchy.

**Réponse exacte :**
A

**Explication courte :**
Split	a	column	of	text	(Power	Query)
You	can	split	a	column	with	a	text	data	type	into	two	or	more	columns	by	using	a	common	delimiter	character.
For	example,	a	Name	column	that	contains	values	written	as	<LastName>,	<FirstName>	can	be	split	into	two
columns	using	the	comma	(,)	character.
Note:	Power	Query	is	an	Extract	Transform	Load	(ETL)	tool.	It	allows	us	to
Download	and	fetch	data	from	different	sources.	We	call	this	data	ingestion
Combine,	clean,	and	model	this	data.	We	call	this	data	wrangling
Reference:
https://support.microsoft.com/en-us/office/split-a-column-of-text-power-query-5282d425-6dd0-46ca-95bf-
8e0da9539662
DRAG	DROP	-
You	need	create	a	date	table	in	Power	BI	that	must	contain	10	full	calendar	years,	including	the	current	year.
How	should	you	complete	the	DAX	expression?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:
Explanation:
Box	1:	
YEAR	-
Get	the	current	year.
Box	2:	
TODAY	-
TODAY	returns	the	current	date.
Box	3:	
CALENDAR	-
CALENDAR	returns	a	table	with	a	single	column	named	Date	containing	a	contiguous	set	of	dates.	The	range

---

## Question 83
**Énoncé de la question :**
8e0da9539662
DRAG	DROP	-
You	need	create	a	date	table	in	Power	BI	that	must	contain	10	full	calendar	years,	including	the	current	year.
How	should	you	complete	the	DAX	expression?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:
Explanation:
Box	1:	
YEAR	-
Get	the	current	year.
Box	2:	
TODAY	-
TODAY	returns	the	current	date.
Box	3:	
CALENDAR	-
CALENDAR	returns	a	table	with	a	single	column	named	Date	containing	a	contiguous	set	of	dates.	The	range

**Réponse exacte :**
B

**Explication courte :**
You	can't	use	USERELATIONSHIP()	to	filter	on	an	active	relationship,	but	need	additional	innactive
relationships
Instead:	Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to
create	Order	Date	and	Delivery	Date	as	calculated	tables.
Reference:
https://docs.microsoft.com/en-us/power-bi/guidance/relationships-active-inactive

---

## Question 85
**Énoncé de la question :**
HOTSPOT	-
You	have	a	Power	BI	report	that	contains	a	measure	named	Total	Sales.
You	need	to	create	a	new	measure	that	will	return	the	sum	of	Total	Sales	for	a	year	up	to	a	selected	date.
How	should	you	complete	the	DAX	expression?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:
	TOTALYTD	-
TOTALYTD	evaluates	the	specified	expression	over	the	interval	which	begins	on	the	first	day	of	the	year	and
ends	with	the	last	date	in	the	specified	date	column	after	applying	specified	filters.
Syntax:	TOTALYTD	(
<Expression>,
<Dates>
[,	<Filter>]
[,	<YearEndDate>]
Expression	-	The	expression	to	be	evaluated.
Dates	-	The	name	of	a	column	containing	dates	or	a	one	column	table	containing	dates.
Example:
TOTALYTD	(	--	2007-01-01	:	2007-05-12
[Sales	Amount],
'Date'[Date]
Box	2:	'
Date'[Date]
Reference:
https://dax.guide/totalytd/
DRAG	DROP	-
You	are	modifying	a	Power	BI	model	by	using	Power	BI	Desktop.
You	have	a	table	named	Sales	that	contains	the	following	fields.
You	have	a	table	named	Transaction	Size	that	contains	the	following	data.
You	need	to	create	a	calculated	column	to	classify	each	transaction	as	small,	medium,	or	large	based	on	the	value
in	Sales	Amount.
How	should	you	complete	the	code?	To	answer,	drag	the	appropriate	values	to	the	correct	targets.	Each	value	may
be	used	once,	more	than	once,	or	not	at	all.
You	may	need	to	drag	the	split	bar	between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:

---

## Question 87
**Énoncé de la question :**
DRAG	DROP	-
You	are	modifying	a	Power	BI	model	by	using	Power	BI	Desktop.
You	have	a	table	named	Sales	that	contains	the	following	fields.
You	have	a	table	named	Transaction	Size	that	contains	the	following	data.
You	need	to	create	a	calculated	column	to	classify	each	transaction	as	small,	medium,	or	large	based	on	the	value
in	Sales	Amount.
How	should	you	complete	the	code?	To	answer,	drag	the	appropriate	values	to	the	correct	targets.	Each	value	may
be	used	once,	more	than	once,	or	not	at	all.
You	may	need	to	drag	the	split	bar	between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:
Answer:

**Réponse exacte :**
B

**Explication courte :**
Remove	a	column	that	is	not	used	in	the	visuals	reduces	the	size	of	the	dataset.
Incorrect:
Not	A:	Merging	the	tables	would	increase	the	dataset.
Not	C:	Two	of	the	visuals	need	historical	data.
Not	D:	Grouping	would	not	affect	size.
You	have	a	Power	BI	report	for	the	marketing	department.	The	report	reports	on	web	traffic	to	a	blog	and	contains
data	from	the	following	tables.

---

## Question 88
**Énoncé de la question :**
Remove	a	column	that	is	not	used	in	the	visuals	reduces	the	size	of	the	dataset.
Incorrect:
Not	A:	Merging	the	tables	would	increase	the	dataset.
Not	C:	Two	of	the	visuals	need	historical	data.
Not	D:	Grouping	would	not	affect	size.
You	have	a	Power	BI	report	for	the	marketing	department.	The	report	reports	on	web	traffic	to	a	blog	and	contains
data	from	the	following	tables.

**Réponse exacte :**
BD

**Explication courte :**
B:	Only	blog	posts	rows	are	useful	for	the	visuals.
D:	These	two	columns	are	not	used	in	the	visuals	and	can	be	removed.
Incorrect:
Not	A:	Three	visuals	need	historical	data.
Not	C:	Traffic[Referring	URL]	is	used	in	one	of	the	visuals	and	therefore	cannot	be	removed.
Not	E:	These	rows	are	used	in	3	visuals.

---

## Question 89
**Énoncé de la question :**
B:	Only	blog	posts	rows	are	useful	for	the	visuals.
D:	These	two	columns	are	not	used	in	the	visuals	and	can	be	removed.
Incorrect:
Not	A:	Three	visuals	need	historical	data.
Not	C:	Traffic[Referring	URL]	is	used	in	one	of	the	visuals	and	therefore	cannot	be	removed.
Not	E:	These	rows	are	used	in	3	visuals.
HOTSPOT
-
You	are	creating	a	quick	measure	as	shown	in	the	following	exhibit.
You	need	to	create	a	monthly	rolling	average	measure	for	Sales	over	time.
How	should	you	configure	the	quick	measure	calculation?	To	answer,	select	the	appropriate	options	in	the	answer
area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
1.	Total	Sales;
2.	Date;
3.	Months
You	have	the	Power	BI	data	model	shown	in	the	following	exhibit.

---

## Question 90
**Énoncé de la question :**
1.	Total	Sales;
2.	Date;
3.	Months
You	have	the	Power	BI	data	model	shown	in	the	following	exhibit.

**Réponse exacte :**
C

**Explication courte :**
Calculate	(SUM(Sales[Sales]),	SAMEPERIODLASTYEAR(dimDate[Date]	))
You	use	Power	BI	Desktop	to	load	data	from	a	Microsoft	SQL	Server	database.
While	waiting	for	the	data	to	load,	you	receive	the	following	error.
You	need	to	resolve	the	error.
What	are	two	ways	to	achieve	the	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Reduce	the	number	of	rows	and	columns	returned	by	each	query.

---

## Question 91
**Énoncé de la question :**
Calculate	(SUM(Sales[Sales]),	SAMEPERIODLASTYEAR(dimDate[Date]	))
You	use	Power	BI	Desktop	to	load	data	from	a	Microsoft	SQL	Server	database.
While	waiting	for	the	data	to	load,	you	receive	the	following	error.
You	need	to	resolve	the	error.
What	are	two	ways	to	achieve	the	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Reduce	the	number	of	rows	and	columns	returned	by	each	query.

**Réponse exacte :**
AB

**Explication courte :**
A.	Reduce	the	number	of	rows	and	columns	returned	by	each	query.
B.	Split	log	running	queries	into	subsets	of	columns	and	use	Power	Query	to	merge	the	queries.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.
The	IoT	GUID	and	IoT	ID	columns	are	unique	to	each	row	in	the	query.
You	need	to	analyze	IoT	events	by	the	hour	and	day	of	the	year.	The	solution	must	improve	dataset	performance.
Solution:	You	split	the	IoT	DateTime	column	into	a	column	named	Date	and	a	column	named	Time.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
A
Explanation:
The	correct	answer	is	A.	Splitting	datetime	column	will	improve	the	performance	even	if	it	generates	one
more	column,	having	less	unique	values	in	separated	date	and	time	columns	will	achieve	better	compression.

---

## Question 92
**Énoncé de la question :**
A.	Reduce	the	number	of	rows	and	columns	returned	by	each	query.
B.	Split	log	running	queries	into	subsets	of	columns	and	use	Power	Query	to	merge	the	queries.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.
The	IoT	GUID	and	IoT	ID	columns	are	unique	to	each	row	in	the	query.
You	need	to	analyze	IoT	events	by	the	hour	and	day	of	the	year.	The	solution	must	improve	dataset	performance.
Solution:	You	split	the	IoT	DateTime	column	into	a	column	named	Date	and	a	column	named	Time.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
A
Explanation:
The	correct	answer	is	A.	Splitting	datetime	column	will	improve	the	performance	even	if	it	generates	one
more	column,	having	less	unique	values	in	separated	date	and	time	columns	will	achieve	better	compression.

**Réponse exacte :**
A

**Explication courte :**
yes	is	a	correct.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.

---

## Question 94
**Énoncé de la question :**
yes	is	a	correct.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.

**Réponse exacte :**
B

**Explication courte :**
B	is	correct	because	changing	the	IoT	DateTime	column	to	the	Date	data	type	alone	will	not	meet	the	goal	of
analyzing	IoT	events	by	the	hour	and	day	of	the	year	in	power	query.
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.
Users	say	that	the	report	is	slow	to	load	the	visuals	when	they	access	and	interact	with	the	report.
You	need	to	recommend	a	solution	to	improve	the	performance	of	the	report.
What	should	you	recommend?
A.	
Change	any	DAX	measures	to	use	iterator	functions.
B.	
Remove	unused	columns	from	tables	in	the	data	model.
C.	
Replace	the	default	visuals	with	AppSource	visuals.
D.	
Increase	the	number	of	times	that	the	dataset	is	refreshed.
Answer:	
B

---

## Question 95
**Énoncé de la question :**
B	is	correct	because	changing	the	IoT	DateTime	column	to	the	Date	data	type	alone	will	not	meet	the	goal	of
analyzing	IoT	events	by	the	hour	and	day	of	the	year	in	power	query.
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.
Users	say	that	the	report	is	slow	to	load	the	visuals	when	they	access	and	interact	with	the	report.
You	need	to	recommend	a	solution	to	improve	the	performance	of	the	report.
What	should	you	recommend?
A.	
Change	any	DAX	measures	to	use	iterator	functions.
B.	
Remove	unused	columns	from	tables	in	the	data	model.
C.	
Replace	the	default	visuals	with	AppSource	visuals.
D.	
Increase	the	number	of	times	that	the	dataset	is	refreshed.
Answer:	
B

**Réponse exacte :**


**Explication courte :**
B	is	correct.	from	performance	point	of	view	its	always	good	to	drop	unwanted	columns.	Avoid	complicated
DAX	and	iterator	functions	as	much	as	possible
DRAG	DROP
-
You	have	a	Power	BI	data	model	that	contains	two	tables	named	Products	and	Sales.
A	one-to-many	relationship	exists	between	the	tables.
You	have	a	report	that	contains	a	report-level	filter	for	Products.
You	need	to	create	a	measure	that	will	return	the	percent	of	total	sales	for	each	product.	The	measure	must
respect	the	report-level	filter	when	calculating	the	total.
How	should	you	complete	the	DAX	measure?	To	answer,	drag	the	appropriate	DAX	functions	to	the	correct
targets.	Each	function	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between
panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
1.Calculate
2.	ALLSELECTED.
ALLSELECTED	Removes	only	the	filter	on	the	expression	visual	but	respect	all	external	filters.
You	have	a	Power	BI	data	model	that	analyzes	product	sales	over	time.	The	data	model	contains	the	following
tables.

---

## Question 97
**Énoncé de la question :**
B	is	correct.	from	performance	point	of	view	its	always	good	to	drop	unwanted	columns.	Avoid	complicated
DAX	and	iterator	functions	as	much	as	possible
DRAG	DROP
-
You	have	a	Power	BI	data	model	that	contains	two	tables	named	Products	and	Sales.
A	one-to-many	relationship	exists	between	the	tables.
You	have	a	report	that	contains	a	report-level	filter	for	Products.
You	need	to	create	a	measure	that	will	return	the	percent	of	total	sales	for	each	product.	The	measure	must
respect	the	report-level	filter	when	calculating	the	total.
How	should	you	complete	the	DAX	measure?	To	answer,	drag	the	appropriate	DAX	functions	to	the	correct
targets.	Each	function	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between
panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
1.Calculate
2.	ALLSELECTED.
ALLSELECTED	Removes	only	the	filter	on	the	expression	visual	but	respect	all	external	filters.
You	have	a	Power	BI	data	model	that	analyzes	product	sales	over	time.	The	data	model	contains	the	following
tables.

**Réponse exacte :**
AC

**Explication courte :**
AC	is	the	correct	answer.	B	is	not	needed	as:	It's	important	to	note	that	when	you	specify	your	own	date	table,
Power	BI	Desktop	does	not	auto-create	the	hierarchies	that	it	would	otherwise	build	into	your	model	on	your
behalf.	If	you	later	deselect	your	date	table	(and	no	longer	have	a	manually	set	date	table),	Power	BI	Desktop
recreates	the	automatically	created	built-in	date	tables	for	you,	for	the	date	columns	in	the	table.
https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-date-tables
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.

---

## Question 98
**Énoncé de la question :**
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.

**Réponse exacte :**
B

**Explication courte :**
Remove	unused	columns	from	tables	in	the	data	model.

---

## Question 99
**Énoncé de la question :**
Remove	unused	columns	from	tables	in	the	data	model.
HOTSPOT
-
You	have	a	Power	BI	data	model	that	contains	a	table	named	Stores.	The	table	has	the	following	columns:
•	Store	Name
•	Open	Date
•	Status
•	State
•	City
You	need	to	create	a	calculated	column	named	Active	Store	Name	that	meets	the	following	requirements:
•	When	the	value	of	the	Status	column	is	“A”,	the	value	in	the	Store	Name	column	must	be	returned.
•	When	the	value	of	the	Status	column	is	NOT	“A”,	the	value	in	the	Store	Name	column	that	is	prefixed	with
"Inactive	-	"	must	be	returned.
How	should	you	complete	the	DAX	expression?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
IF

**Réponse exacte :**
C

**Explication courte :**
Answer	is	C	and	not	B	because	the	conditional	column	would	be	year	and	not	the	logged	date,	also	the	data
type	should	be	date	not	whole	number	as	specified	in	B.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.
The	IoT	GUID	and	IoT	ID	columns	are	unique	to	each	row	in	the	query.
You	need	to	analyze	IoT	events	by	the	hour	and	day	of	the	year.	The	solution	must	improve	dataset	performance.

---

## Question 101
**Énoncé de la question :**
Answer	is	C	and	not	B	because	the	conditional	column	would	be	year	and	not	the	logged	date,	also	the	data
type	should	be	date	not	whole	number	as	specified	in	B.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
From	Power	Query	Editor,	you	profile	the	data	shown	in	the	following	exhibit.
The	IoT	GUID	and	IoT	ID	columns	are	unique	to	each	row	in	the	query.
You	need	to	analyze	IoT	events	by	the	hour	and	day	of	the	year.	The	solution	must	improve	dataset	performance.

**Réponse exacte :**
B

**Explication courte :**
Answer	is	NO.
IoT	GUID	&	IOT	ID	both	are	unique	key	columns.	so	we	can	delete	any	one	among	them.	From	performance
point	of	view	its	good	to	delete	text	ID	column	i.e	IOT	GUID	and	keep	IOT	ID.	concatenation	is	not	required
Both	are	unique	columns,	but	by	concatenating	them	you	will	end	up	with	a	Unique	Key	with	data	type	Text.
This	raises	performance	issues	since	Unique	keys	should	be	preferably	integers	for	performance	reasons.
Also,	since	IoT	GUID	is	not	required	might	as	well	remove	it.
You	have	a	Power	BI	model	that	contains	a	table	named	Employee.	The	table	contains	the	following	data.
Each	employee	has	one	manager	as	shown	in	the	ParentEmployeeID	column.
All	reporting	paths	lead	to	the	CEO	at	the	top	of	the	organizational	hierarchy.
You	need	to	create	a	calculated	column	that	returns	the	count	of	levels	from	each	employee	to	the	CEO.
Which	DAX	expression	should	you	use?
A.	
PATHLENGTH(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]))
B.	
PATHITEM(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]),1,INTEGER)
C.	
PATHCONTAINS(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]),1)
D.	
PATH(Employee[EmployeeID],Employee[ParentEmployeeID])
Answer:	
A

---

## Question 102
**Énoncé de la question :**
Answer	is	NO.
IoT	GUID	&	IOT	ID	both	are	unique	key	columns.	so	we	can	delete	any	one	among	them.	From	performance
point	of	view	its	good	to	delete	text	ID	column	i.e	IOT	GUID	and	keep	IOT	ID.	concatenation	is	not	required
Both	are	unique	columns,	but	by	concatenating	them	you	will	end	up	with	a	Unique	Key	with	data	type	Text.
This	raises	performance	issues	since	Unique	keys	should	be	preferably	integers	for	performance	reasons.
Also,	since	IoT	GUID	is	not	required	might	as	well	remove	it.
You	have	a	Power	BI	model	that	contains	a	table	named	Employee.	The	table	contains	the	following	data.
Each	employee	has	one	manager	as	shown	in	the	ParentEmployeeID	column.
All	reporting	paths	lead	to	the	CEO	at	the	top	of	the	organizational	hierarchy.
You	need	to	create	a	calculated	column	that	returns	the	count	of	levels	from	each	employee	to	the	CEO.
Which	DAX	expression	should	you	use?
A.	
PATHLENGTH(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]))
B.	
PATHITEM(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]),1,INTEGER)
C.	
PATHCONTAINS(PATH(Employee[EmployeeID],Employee[ParentEmployeeID]),1)
D.	
PATH(Employee[EmployeeID],Employee[ParentEmployeeID])
Answer:	
A

**Réponse exacte :**


**Explication courte :**
The	Answer	is	A	because	the	question	instructs	that	we	count	the	different	levels	of	each	employee.	The
PathLength	gives	the	result.	For	more	information	see	the	link	https://learn.microsoft.com/en-
us/dax/pathlength-function-dax
Although	for	CEO	it	returns	1	-	so	I	personally	would	substract	1	from	this	PATHLENGTH	when	creating	the
report,	as	I	think	numbers	of	levels	from	CEO	to	CEO	is	0,	formanagaers	directly	under	CEO	it	is	1	etc
Answer	D	is	wrong	because	it	only	returns	the	items	related	to	the	current	row	value	and	does	not	give	the
count.
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.
Users	say	that	the	report	is	slow	to	load	the	visuals	when	they	access	and	interact	with	the	report.
You	need	to	recommend	a	solution	to	improve	the	performance	of	the	report.
What	should	you	recommend?
A.	
Replace	the	default	visuals	with	AppSource	visuals.
B.	
Remove	unused	columns	from	tables	in	the	data	model.
C.	
Change	the	imported	dataset	to	DirectQuery
D.	
Increase	the	number	of	times	that	the	dataset	is	refreshed.
Answer:	
B
Explanation:
B	is	correct	Removing	unwanted	columns	from	the	data	model	is	a	good	trick	to	improve	the	performance.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.	
Change	the	data	type	of	the	Logged	column	to	Date.
B.	
Split	the	Logged	column	by	using	at	as	the	delimiter.
C.	
Add	a	conditional	column	that	outputs	2018	if	the	Logged	column	starts	with	2018	and	set	the	data	type	of
the	new	column	to	Whole	Number.
D.	
Apply	the	Parse	function	from	the	Date	transformations	options	to	the	Logged	column.

---

## Question 104
**Énoncé de la question :**
us/dax/pathlength-function-dax
Although	for	CEO	it	returns	1	-	so	I	personally	would	substract	1	from	this	PATHLENGTH	when	creating	the
report,	as	I	think	numbers	of	levels	from	CEO	to	CEO	is	0,	formanagaers	directly	under	CEO	it	is	1	etc
Answer	D	is	wrong	because	it	only	returns	the	items	related	to	the	current	row	value	and	does	not	give	the
count.
You	have	a	Microsoft	Power	BI	report.	The	size	of	PBIX	file	is	550	MB.	The	report	is	accessed	by	using	an	App
workspace	in	shared	capacity	of	powerbi.com.
The	report	uses	an	imported	dataset	that	contains	one	fact	table.	The	fact	table	contains	12	million	rows.	The
dataset	is	scheduled	to	refresh	twice	a	day	at	08:00	and	17:00.
The	report	is	a	single	page	that	contains	15	AppSource	visuals	and	10	default	visuals.
Users	say	that	the	report	is	slow	to	load	the	visuals	when	they	access	and	interact	with	the	report.
You	need	to	recommend	a	solution	to	improve	the	performance	of	the	report.
What	should	you	recommend?
A.	
Replace	the	default	visuals	with	AppSource	visuals.
B.	
Remove	unused	columns	from	tables	in	the	data	model.
C.	
Change	the	imported	dataset	to	DirectQuery
D.	
Increase	the	number	of	times	that	the	dataset	is	refreshed.
Answer:	
B
Explanation:
B	is	correct	Removing	unwanted	columns	from	the	data	model	is	a	good	trick	to	improve	the	performance.
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.	
Change	the	data	type	of	the	Logged	column	to	Date.
B.	
Split	the	Logged	column	by	using	at	as	the	delimiter.
C.	
Add	a	conditional	column	that	outputs	2018	if	the	Logged	column	starts	with	2018	and	set	the	data	type	of
the	new	column	to	Whole	Number.
D.	
Apply	the	Parse	function	from	the	Date	transformations	options	to	the	Logged	column.

**Réponse exacte :**
B

**Explication courte :**
C	refers	to	a	whole	number	as	data	type	which	can't	be	used	as	a	date	hierarchy,
	
​
so	B	is	the	only	right	answer.

---

## Question 105
**Énoncé de la question :**
C	refers	to	a	whole	number	as	data	type	which	can't	be	used	as	a	date	hierarchy,
	
​
so	B	is	the	only	right	answer.
HOTSPOT
-
You	have	the	Power	BI	data	model	shown	in	the	following	exhibit.
You	need	to	create	a	measure	to	count	the	number	of	product	categories	that	had	products	sold	during	a	selected
period.
How	should	you	complete	the	DAX	expression?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
Distinctcount('Product'[product	category],
'sales'
We	have	to	count	the	distinct	number	of	categories	in	the	product	table	and	then	use	the	filter	'sales'	so	it	will

**Réponse exacte :**
D

**Explication courte :**
Remove	unused	columns	from	tables	in	the	data	model.

---

## Question 107
**Énoncé de la question :**
Remove	unused	columns	from	tables	in	the	data	model.
HOTSPOT
-
You	have	the	Power	BI	data	model	shown	in	the	following	exhibit.
The	Sales	table	has	the	following	columns.

**Réponse exacte :**


**Explication courte :**
Yes
No
Yes
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Create	a	column	by	example	that	starts	with	2018-12-31	and	set	the	data	type	of	the	new	column	to	Date
B.
Create	a	column	by	example	that	starts	with	2018-12-31
C.
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column
D.
Add	a	conditional	column	that	outputs	2018	if	the	Logged	column	starts	with	2018	and	set	the	data	type	of
the	new	column	to	Whole	Number
Answer:	
A
Explanation:
Create	a	column	by	example	that	starts	with	2018-12-31	and	set	the	data	type	of	the	new	column	to	Date
You	have	a	Power	BI	data	model	that	contains	a	table	named	Employees.	The	table	has	the	following	columns:
•Employee	Name
•Email	Address
•Start	Date
•Job	Title
You	are	implementing	dynamic	row-level	security	(RLS).
You	need	to	create	a	table	filter	to	meet	the	following	requirements:
•Users	must	see	only	their	own	employee	data.
•The	DAX	expression	must	work	in	both	Power	BI	Desktop	and	the	Power	BI	service.
Which	expression	should	you	use?
A.
[Email	Address]	-	USERNAME()
B.
[Employee	Name]	-	USERPRINCIPALNAME()
C.
[Employee	Name]	=	USERNAME()
D.
[Email	Address]	=	USERPRINCIPALNAME()
Answer:	
D
Explanation:
To	implement	dynamic	row-level	security	(RLS)	on	the	Employees	table,	a	table	filter	must	be	created.	The
table	filter	should	be	based	on	the	user's	email	address	or	user	principal	name	(UPN),	as	these	are	unique
identifiers	for	each	user.The	DAX	expression	[Email	Address]	=	USERPRINCIPALNAME()	will	filter	the
Employees	table	to	only	show	rows	where	the	Email	Address	column	matches	the	UPN	of	the	current	user.
This	expression	works	in	both	Power	BI	Desktop	and	the	Power	BI	service,	and	will	ensure	that	each	user	only
sees	their	own	employee	data.

---

## Question 110
**Énoncé de la question :**
Yes
No
Yes
You	have	a	CSV	file	that	contains	user	complaints.	The	file	contains	a	column	named	Logged.	Logged	contains	the
date	and	time	each	complaint	occurred.	The	data	in	Logged	is	in	the	following	format:	2018-12-31	at	08:59.
You	need	to	be	able	to	analyze	the	complaints	by	the	logged	date	and	use	a	built-in	date	hierarchy.
What	should	you	do?
A.
Create	a	column	by	example	that	starts	with	2018-12-31	and	set	the	data	type	of	the	new	column	to	Date
B.
Create	a	column	by	example	that	starts	with	2018-12-31
C.
Apply	a	transformation	to	extract	the	last	11	characters	of	the	Logged	column
D.
Add	a	conditional	column	that	outputs	2018	if	the	Logged	column	starts	with	2018	and	set	the	data	type	of
the	new	column	to	Whole	Number
Answer:	
A
Explanation:
Create	a	column	by	example	that	starts	with	2018-12-31	and	set	the	data	type	of	the	new	column	to	Date
You	have	a	Power	BI	data	model	that	contains	a	table	named	Employees.	The	table	has	the	following	columns:
•Employee	Name
•Email	Address
•Start	Date
•Job	Title
You	are	implementing	dynamic	row-level	security	(RLS).
You	need	to	create	a	table	filter	to	meet	the	following	requirements:
•Users	must	see	only	their	own	employee	data.
•The	DAX	expression	must	work	in	both	Power	BI	Desktop	and	the	Power	BI	service.
Which	expression	should	you	use?
A.
[Email	Address]	-	USERNAME()
B.
[Employee	Name]	-	USERPRINCIPALNAME()
C.
[Employee	Name]	=	USERNAME()
D.
[Email	Address]	=	USERPRINCIPALNAME()
Answer:	
D
Explanation:
To	implement	dynamic	row-level	security	(RLS)	on	the	Employees	table,	a	table	filter	must	be	created.	The
table	filter	should	be	based	on	the	user's	email	address	or	user	principal	name	(UPN),	as	these	are	unique
identifiers	for	each	user.The	DAX	expression	[Email	Address]	=	USERPRINCIPALNAME()	will	filter	the
Employees	table	to	only	show	rows	where	the	Email	Address	column	matches	the	UPN	of	the	current	user.
This	expression	works	in	both	Power	BI	Desktop	and	the	Power	BI	service,	and	will	ensure	that	each	user	only
sees	their	own	employee	data.

**Réponse exacte :**


**Explication courte :**
[Email]	=	userprincipalname()	for	Human	Resources	and	[Manager	=	[CFO]	for	Country.
You	have	a	Power	BI	data	model	that	imports	data	from	a	Microsoft	Excel	spreadsheet.
You	use	Power	Query	to	load	a	query	that	contains	both	renamed	and	custom	columns.
Later,	you	attempt	to	reload	the	query	and	receive	the	following	error	message.
Expression.Error:	The	column	'Category'	of	the	table	wasn't	found.
What	are	two	possible	causes	of	the	error?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
The	column	was	removed	from	the	source	file.
B.	
The	column	was	renamed	in	the	source	file.

---

## Question 111
**Énoncé de la question :**
[Email]	=	userprincipalname()	for	Human	Resources	and	[Manager	=	[CFO]	for	Country.
You	have	a	Power	BI	data	model	that	imports	data	from	a	Microsoft	Excel	spreadsheet.
You	use	Power	Query	to	load	a	query	that	contains	both	renamed	and	custom	columns.
Later,	you	attempt	to	reload	the	query	and	receive	the	following	error	message.
Expression.Error:	The	column	'Category'	of	the	table	wasn't	found.
What	are	two	possible	causes	of	the	error?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
The	column	was	removed	from	the	source	file.
B.	
The	column	was	renamed	in	the	source	file.

**Réponse exacte :**
AB

**Explication courte :**
A.	The	column	was	removed	from	the	source	file.
B.	The	column	was	renamed	in	the	source	file.
You	have	a	Power	BI	model	that	contains	a	table	named	Sales.	The	Sales	table	contains	the	following	columns:
•Order	Line	ID
•Product	ID
•Unit	Price
•Order	ID
•Quantity
Orders	are	uniquely	identified	by	using	the	order	ID	and	can	have	multiple	order	lines.	Each	order	line	within	an
order	contains	a	different	product	ID.
You	need	to	write	a	DAX	measure	that	counts	the	number	of	orders.
Which	formula	should	you	use?
A.
Count('Sales'[Order	ID])
B.
CountA('Sales'	[Order	ID])
C.
CountRows('Sales')
D.
DistinctCount('Sales'	[Order	ID])
Answer:	
D
Explanation:
Orders	are	uniquely	identified	by	using	the	order	ID	and	can	have	multiple	order	lines"	-	I	think	the	important
statement	is	"and	can	have	multiple	order	lines"	which	means	that	the	order	ID	can	appear	more	than	once	in
the	table	if	the	order	contains	more	than	one	products.

---

## Question 113
**Énoncé de la question :**
A.	The	column	was	removed	from	the	source	file.
B.	The	column	was	renamed	in	the	source	file.
You	have	a	Power	BI	model	that	contains	a	table	named	Sales.	The	Sales	table	contains	the	following	columns:
•Order	Line	ID
•Product	ID
•Unit	Price
•Order	ID
•Quantity
Orders	are	uniquely	identified	by	using	the	order	ID	and	can	have	multiple	order	lines.	Each	order	line	within	an
order	contains	a	different	product	ID.
You	need	to	write	a	DAX	measure	that	counts	the	number	of	orders.
Which	formula	should	you	use?
A.
Count('Sales'[Order	ID])
B.
CountA('Sales'	[Order	ID])
C.
CountRows('Sales')
D.
DistinctCount('Sales'	[Order	ID])
Answer:	
D
Explanation:
Orders	are	uniquely	identified	by	using	the	order	ID	and	can	have	multiple	order	lines"	-	I	think	the	important
statement	is	"and	can	have	multiple	order	lines"	which	means	that	the	order	ID	can	appear	more	than	once	in
the	table	if	the	order	contains	more	than	one	products.
HOTSPOT
-
You	are	creating	a	Power	BI	model	in	Power	BI	Desktop.
You	need	to	create	a	calculated	table	named	Numbers	that	will	contain	all	the	integers	from	-100	to	100.
How	should	you	complete	the	DAX	calculation?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
To	create	a	calculated	table	named	Numbers	in	Power	BI	Desktop	that	contains	all	the	integers	from	-100	to
100,	you	can	use	the	following	DAX	calculation:	Numbers	=	
GENERATESERIES(-100,	100,	1)
The	GENERATESERIES	function	generates	a	table	of	values	that	starts	at	the	first	argument	(-100),	ends	at
the	second	argument	(100),	and	increments	by	the	third	argument	(1)	in	this	case.	The	resulting	table	will
contain	all	the	integers	from	-100	to	100	inclusive.	The	calculated	table	is	named	"Numbers"	and	is	created	by
assigning	the	output	of	the	GENERATESERIES	function	to	it	using	the	"="	operator.	No	confusion,	and	no	need
to	discuss	further
You	have	a	Power	BI	data	model	that	contains	a	table	named	Employees.	The	table	has	the	following	columns:
•Employee	Name
•Email	Address
•Start	Date
•Job	Title
You	are	implementing	dynamic	row-level	security	(RLS).
You	need	to	create	a	table	filter	to	meet	the	following	requirements:
•Users	must	see	only	their	own	employee	data.
•The	DAX	expression	must	work	in	both	Power	BI	Desktop	and	the	Power	BI	service.
Which	expression	should	you	use?
A.
[Employee	Name]	=	USERPRINCIPALNAME()

---

## Question 114
**Énoncé de la question :**
To	create	a	calculated	table	named	Numbers	in	Power	BI	Desktop	that	contains	all	the	integers	from	-100	to
100,	you	can	use	the	following	DAX	calculation:	Numbers	=	
GENERATESERIES(-100,	100,	1)
The	GENERATESERIES	function	generates	a	table	of	values	that	starts	at	the	first	argument	(-100),	ends	at
the	second	argument	(100),	and	increments	by	the	third	argument	(1)	in	this	case.	The	resulting	table	will
contain	all	the	integers	from	-100	to	100	inclusive.	The	calculated	table	is	named	"Numbers"	and	is	created	by
assigning	the	output	of	the	GENERATESERIES	function	to	it	using	the	"="	operator.	No	confusion,	and	no	need
to	discuss	further
You	have	a	Power	BI	data	model	that	contains	a	table	named	Employees.	The	table	has	the	following	columns:
•Employee	Name
•Email	Address
•Start	Date
•Job	Title
You	are	implementing	dynamic	row-level	security	(RLS).
You	need	to	create	a	table	filter	to	meet	the	following	requirements:
•Users	must	see	only	their	own	employee	data.
•The	DAX	expression	must	work	in	both	Power	BI	Desktop	and	the	Power	BI	service.
Which	expression	should	you	use?
A.
[Employee	Name]	=	USERPRINCIPALNAME()

**Réponse exacte :**
D

**Explication courte :**
The	correct	answer	is	D.	[Email	Address]	=	USERPRINCIPALNAME().	The	expression	checks	the	email	address
of	the	currently	logged-in	user	against	the	email	address	in	the	Employees	table,	which	should	be	used	as	the
identifier	for	each	employee.	This	will	ensure	that	each	user	can	only	see	their	own	employee	data.	The	other
options	may	not	work	in	all	cases,	as	the	username	and	user	principal	name	may	not	always	match	the	email
address	used	as	the	identifier.
You	have	a	Power	BI	model	that	contains	a	table	named	Date.	The	Date	table	contains	the	following	columns:
•Date
•Fiscal	Year
•Fiscal	Quarter
•Month	Name
•Calendar	Year
•Week	Number
•Month	Number
•Calendar	Quarter
You	need	to	create	a	calculated	table	based	on	the	Date	table.	The	calculated	table	must	contain	only	unique
combinations	of	values	for	Calendar	Year,	Calendar	Quarter,	and	Calendar	Month.
Which	DAX	function	should	you	include	in	the	table	definition?
A.
ADDCOLUMNS
B.
CALCULATE
C.
SUMMARIZE
D.
DATATABLE
Answer:	
C
Explanation:
SUMMARIZE	SUMMARIZE:"	Creates	a	summary	of	the	input	table	grouped	by	the	specified	columns.
"ADDCOLUMNS:"	Returns	a	table	with	new	columns	specified	by	the	DAX	expressions."	Based	on	this,	using
SUMMARIZE	will	give	us	the	unique	combination	we	want	and	don't	need	to	use	DAX	expressions	to	create
the	calculated	table.

---

## Question 116
**Énoncé de la question :**
The	correct	answer	is	D.	[Email	Address]	=	USERPRINCIPALNAME().	The	expression	checks	the	email	address
of	the	currently	logged-in	user	against	the	email	address	in	the	Employees	table,	which	should	be	used	as	the
identifier	for	each	employee.	This	will	ensure	that	each	user	can	only	see	their	own	employee	data.	The	other
options	may	not	work	in	all	cases,	as	the	username	and	user	principal	name	may	not	always	match	the	email
address	used	as	the	identifier.
You	have	a	Power	BI	model	that	contains	a	table	named	Date.	The	Date	table	contains	the	following	columns:
•Date
•Fiscal	Year
•Fiscal	Quarter
•Month	Name
•Calendar	Year
•Week	Number
•Month	Number
•Calendar	Quarter
You	need	to	create	a	calculated	table	based	on	the	Date	table.	The	calculated	table	must	contain	only	unique
combinations	of	values	for	Calendar	Year,	Calendar	Quarter,	and	Calendar	Month.
Which	DAX	function	should	you	include	in	the	table	definition?
A.
ADDCOLUMNS
B.
CALCULATE
C.
SUMMARIZE
D.
DATATABLE
Answer:	
C
Explanation:
SUMMARIZE	SUMMARIZE:"	Creates	a	summary	of	the	input	table	grouped	by	the	specified	columns.
"ADDCOLUMNS:"	Returns	a	table	with	new	columns	specified	by	the	DAX	expressions."	Based	on	this,	using
SUMMARIZE	will	give	us	the	unique	combination	we	want	and	don't	need	to	use	DAX	expressions	to	create
the	calculated	table.
HOTSPOT
-
You	have	a	Power	BI	model	that	contains	the	following	data.

**Réponse exacte :**


**Explication courte :**
SUMMARIZE	-	Date[Year]
You	use	Power	Query	Editor	to	import	and	preview	sales	data	from	the	years	2020	and	2021	in	a	Microsoft	Excel
file	as	shown	in	the	following	exhibit.

---

## Question 117
**Énoncé de la question :**
SUMMARIZE	-	Date[Year]
You	use	Power	Query	Editor	to	import	and	preview	sales	data	from	the	years	2020	and	2021	in	a	Microsoft	Excel
file	as	shown	in	the	following	exhibit.

**Réponse exacte :**
C

**Explication courte :**
C	is	correct	assuming	we	are	selecting	the	"2020"	and	"2021"	columns

---

## Question 118
**Énoncé de la question :**
C	is	correct	assuming	we	are	selecting	the	"2020"	and	"2021"	columns
HOTSPOT

**Réponse exacte :**


**Explication courte :**
Calculate
Last	Date
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
•Due	Date
•Order	Date
•Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	three	dates	at	the	same	time.
Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to	create	Order
Date	and	Delivery	Date	as	calculated	tables.	You	create	active	relationships	between	the	sales	table	and	each	date
table.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
A

---

## Question 119
**Énoncé de la question :**
Calculate
Last	Date
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	Power	BI	report	that	imports	a	date	table	and	a	sales	table	from	an	Azure	SQL	database	data	source.
The	sales	table	has	the	following	date	foreign	keys:
•Due	Date
•Order	Date
•Delivery	Date
You	need	to	support	the	analysis	of	sales	over	time	based	on	all	three	dates	at	the	same	time.
Solution:	From	the	Fields	pane,	you	rename	the	date	table	as	Due	Date.	You	use	a	DAX	expression	to	create	Order
Date	and	Delivery	Date	as	calculated	tables.	You	create	active	relationships	between	the	sales	table	and	each	date
table.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
A

**Réponse exacte :**


**Explication courte :**
yes	is	a	correct	answer.

---

## Question 121
**Énoncé de la question :**
yes	is	a	correct	answer.
HOTSPOT
-
You	are	creating	a	Power	BI	report	that	will	show	the	number	of	current	employees	over	time.	The	report	will	use
Import	storage	mode	for	all	tables.
The	employment	data	will	be	imported	from	Azure	SQL	Database	in	a	monthly	snapshot.	The	data	will	be	stored	in
a	table	named	Headcount	and	will	contain	the	following:
•One	row	per	employee	for	each	month	the	employee	is	employed
•In	each	row,	a	date	key	that	shows	the	first	day	of	the	month	of	each	snapshot
You	have	a	related	date	table	that	contains	dates	for	the	years	2020	to	2030.
You	need	to	create	a	semi-additive	DAX	measure	that	will	return	the	count	of	employees	for	the	last	available	date
in	a	year,	quarter,	or	month.
How	should	you	complete	the	measure?	To	answer,	select	the	appropriate	options	in	the	answer	area.
Answer:
Explanation:
Count	Rows	(Headcount)
Last	Date(Date"	(Date)

**Réponse exacte :**
A

**Explication courte :**
DATEADD	is	correct.	PARALLELPERIOD	also	calculate	one	quarter	before,	but	the	out	come	is	the	total	sales
of	three	months	of	previous	quarter	not	only	one	day	or	one	month	of	previous	quarter.

---

## Question 122
**Énoncé de la question :**
DATEADD	is	correct.	PARALLELPERIOD	also	calculate	one	quarter	before,	but	the	out	come	is	the	total	sales
of	three	months	of	previous	quarter	not	only	one	day	or	one	month	of	previous	quarter.

**Réponse exacte :**
D

**Explication courte :**
Correct	answer	is	D:Split	the	visuals	onto	multiple	pages.
You	are	reviewing	a	Power	BI	data	model.
You	have	a	calculated	table	that	has	the	following	definition.
ProductList	=	INTERSECT	(	ProductsGroupA,	ProductsGroupB	)
You	need	to	identify	the	results	of	the	DAX	expression.
Which	rows	will	be	returned	in	ProductList?
A.
all	the	rows	in	ProductsGroupB	that	have	a	matching	row	in	ProductsGroupA
B.
all	the	rows	in	both	tables
C.
all	the	rows	in	ProductsGroupA	that	have	a	matching	row	in	ProductsGroupB
D.
all	the	rows	in	ProductsGroupA	that	have	no	matching	row	in	ProductsGroupB.
Answer:	
C
Explanation:
all	the	rows	in	ProductsGroupA	that	have	a	matching	row	in	ProductsGroupB.
You	have	a	Power	BI	data	model	that	contains	two	tables	named	Sales	and	Date.	The	Sales	table	contains	three

---

## Question 125
**Énoncé de la question :**
Correct	answer	is	D:Split	the	visuals	onto	multiple	pages.
You	are	reviewing	a	Power	BI	data	model.
You	have	a	calculated	table	that	has	the	following	definition.
ProductList	=	INTERSECT	(	ProductsGroupA,	ProductsGroupB	)
You	need	to	identify	the	results	of	the	DAX	expression.
Which	rows	will	be	returned	in	ProductList?
A.
all	the	rows	in	ProductsGroupB	that	have	a	matching	row	in	ProductsGroupA
B.
all	the	rows	in	both	tables
C.
all	the	rows	in	ProductsGroupA	that	have	a	matching	row	in	ProductsGroupB
D.
all	the	rows	in	ProductsGroupA	that	have	no	matching	row	in	ProductsGroupB.
Answer:	
C
Explanation:
all	the	rows	in	ProductsGroupA	that	have	a	matching	row	in	ProductsGroupB.
You	have	a	Power	BI	data	model	that	contains	two	tables	named	Sales	and	Date.	The	Sales	table	contains	three

**Réponse exacte :**
C

**Explication courte :**
Correct	answer	is	C:Values.

---

## Question 126
**Énoncé de la question :**
Correct	answer	is	C:Values.
HOTSPOT
-
You	have	Power	BI	report	that	contains	the	fields	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Two	explicit	measures	.
Summarization	setting.
You	have	a	Power	BI	model	that	contains	a	table	named	Employees.	The	table	contains	the	following	columns:
•Employee	ID
•First	Name
•Last	Name
•Department
•Salary
Each	employee	is	uniquely	identified	by	using	Employee	ID.
You	need	to	create	a	DAX	measure	that	will	calculate	the	average	salary	of	all	the	employees	in	the	sales
department.
Which	DAX	expression	should	you	use?
A.
DISTINCTCOUNT(‘Employees’[Salary])

---

## Question 127
**Énoncé de la question :**
Two	explicit	measures	.
Summarization	setting.
You	have	a	Power	BI	model	that	contains	a	table	named	Employees.	The	table	contains	the	following	columns:
•Employee	ID
•First	Name
•Last	Name
•Department
•Salary
Each	employee	is	uniquely	identified	by	using	Employee	ID.
You	need	to	create	a	DAX	measure	that	will	calculate	the	average	salary	of	all	the	employees	in	the	sales
department.
Which	DAX	expression	should	you	use?
A.
DISTINCTCOUNT(‘Employees’[Salary])

**Réponse exacte :**
C

**Explication courte :**
CALCULATE(AVERAGE(‘Employees’[Salary]),	‘Employees’[Department]	=	“Sales”).
You	use	Power	Query	Editor	to	preview	a	query	that	contains	sales	order	data	in	the	following	columns:
•Tax	Amount
•Sales	Order	ID
•Freight	Amount
•Subtotal	Amount
•Total	Item	Quantity
The	Sales	Order	ID	column	uniquely	identifies	each	sales	order.	The	Subtotal	Amount	and	Total	Item	Quantity
columns	are	always	populated,	but	the	Tax	Amount	and	Freight	Amount	columns	are	sometimes	null	when	an
order	has	no	associated	amount.
You	need	to	query	the	data	to	identify	the	following	metrics	by	month:
•The	average	item	quantity	per	order
•The	average	freight	amount	per	order
•The	maximum	item	quantity	per	order
How	should	you	modify	the	query?
A.
In	the	Total	Item	Quantity	column,	replace	the	null	values	with	0.
B.
In	the	Tax	Amount	column,	remove	rows	that	contain	null	values.
C.
In	the	Freight	Amount	column,	remove	rows	that	contain	null	values.
D.
In	the	Freight	Amount	column,	replace	the	null	values	with	0.
Answer:	
D
Explanation:
In	the	Freight	Amount	column,	replace	the	null	values	with	0.
DRAG	DROP
-
You	use	Power	Query	Editor	to	import	three	tables	named	Customers,	Address,	and	Country.
In	the	source	system,	not	every	customer	has	a	related	address,	but	every	address	has	a	related	country.
You	need	to	merge	all	the	tables	into	a	single	query.	The	solution	must	optimize	query	refresh	performance.
Which	type	of	join	should	you	use	for	each	merge	operation?	To	answer,	drag	the	appropriate	join	types	to	the
correct	operations.	Each	join	type	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split

---

## Question 129
**Énoncé de la question :**
CALCULATE(AVERAGE(‘Employees’[Salary]),	‘Employees’[Department]	=	“Sales”).
You	use	Power	Query	Editor	to	preview	a	query	that	contains	sales	order	data	in	the	following	columns:
•Tax	Amount
•Sales	Order	ID
•Freight	Amount
•Subtotal	Amount
•Total	Item	Quantity
The	Sales	Order	ID	column	uniquely	identifies	each	sales	order.	The	Subtotal	Amount	and	Total	Item	Quantity
columns	are	always	populated,	but	the	Tax	Amount	and	Freight	Amount	columns	are	sometimes	null	when	an
order	has	no	associated	amount.
You	need	to	query	the	data	to	identify	the	following	metrics	by	month:
•The	average	item	quantity	per	order
•The	average	freight	amount	per	order
•The	maximum	item	quantity	per	order
How	should	you	modify	the	query?
A.
In	the	Total	Item	Quantity	column,	replace	the	null	values	with	0.
B.
In	the	Tax	Amount	column,	remove	rows	that	contain	null	values.
C.
In	the	Freight	Amount	column,	remove	rows	that	contain	null	values.
D.
In	the	Freight	Amount	column,	replace	the	null	values	with	0.
Answer:	
D
Explanation:
In	the	Freight	Amount	column,	replace	the	null	values	with	0.
DRAG	DROP
-
You	use	Power	Query	Editor	to	import	three	tables	named	Customers,	Address,	and	Country.
In	the	source	system,	not	every	customer	has	a	related	address,	but	every	address	has	a	related	country.
You	need	to	merge	all	the	tables	into	a	single	query.	The	solution	must	optimize	query	refresh	performance.
Which	type	of	join	should	you	use	for	each	merge	operation?	To	answer,	drag	the	appropriate	join	types	to	the
correct	operations.	Each	join	type	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split

**Réponse exacte :**
You	have	a	Power	BI	semantic	model	that	contains	four	queries	named	Query	1,	Query2.	Query3,	and	Query4.
Query1	loads	customer	data	into	the	model	and	is	referenced	by	the	other	three	queries.
You	discover	that	data	refresh	for	the	model	is	slow.
You	need	to	improve	the	data	refresh	time.	The	solution	must	minimize	costs.
What	should	you	do?
A.
Run	the	Table.buffer	function	in	Query1.
B.
Duplicate	Query1	to	all	the	other	queries.
C.
Reconfigure	Query1	as	a	dataflow	entity.
D.
From	the	Power	BI	Admin	portal,	increase	the	Capacity	settings.
Answer:	
A

**Explication courte :**
Run	the	Table.buffer	function	in	Query1.

---

## Question 132
**Énoncé de la question :**
Run	the	Table.buffer	function	in	Query1.

**Réponse exacte :**
You	have	a	Power	BI	semantic	model	that	connects	to	a	streaming	data	source.	The	data	source	is	updated
frequently.
You	need	to	create	a	Power	BI	report	that	meets	the	following	requirements:
•Supports	real-time	analytics
•Minimizes	performance	impact	on	the	data	source
•Displays	the	most	recent	data	without	performing	a	data	refresh
Which	connectivity	mode	should	you	use	for	the	dataset?
A.
DirectQuery	mode
B.
import	mode
C.
LiveConnect	mode
D.
push	mode
Answer:	
A

**Explication courte :**


---

## Question 137
**Énoncé de la question :**


**Réponse exacte :**
BE

**Explication courte :**
B.DAX	query.
E.Visual	display.
You	have	a	Microsoft	365	subscription	that	contains	the	resources	shown	in	the	following	table.
You	create	a	new	dashboard	that	uses	row-level	security	(RLS)	filters.	You	define	a	new	role	named	Consultants.
To	which	resource	can	you	assign	the	Consultants	role?
A.
Group2
B.
Team1
C.
Sales	reports
D.
Group1
Answer:	
A
Explanation:
Correct	answer	is	A:Group2.

---

## Question 139
**Énoncé de la question :**
B.DAX	query.
E.Visual	display.
You	have	a	Microsoft	365	subscription	that	contains	the	resources	shown	in	the	following	table.
You	create	a	new	dashboard	that	uses	row-level	security	(RLS)	filters.	You	define	a	new	role	named	Consultants.
To	which	resource	can	you	assign	the	Consultants	role?
A.
Group2
B.
Team1
C.
Sales	reports
D.
Group1
Answer:	
A
Explanation:
Correct	answer	is	A:Group2.

**Réponse exacte :**
A

**Explication courte :**
CALCULATE(SUM(Sales[SalesAmount]),	DATEADD(Date[Date],	-30,	DAY))
You	publish	a	semantic	model	to	the	Power	BI	service.	The	semantic	model	contains	data	from	the	following	data
sources:
•Source1:	A	Microsoft	Excel	file	stored	in	Microsoft	OneDrive	for	Business
•Source2:	An	Azure	SQL	database	on	a	virtual	network
•Source3:	A	public	website
Which	data	sources	require	an	on-premises	data	gateway?
A.
Source1	only
B.
Source2	only
C.
Source3	only
D.
Source1	and	Source2	only
E.
Source2	and	Source3	only
F.
Source1,	Source2,	and	Source3
Answer:	
B
Explanation:
Correct	answer	is	B:Source2	only.

---

## Question 141
**Énoncé de la question :**
CALCULATE(SUM(Sales[SalesAmount]),	DATEADD(Date[Date],	-30,	DAY))
You	publish	a	semantic	model	to	the	Power	BI	service.	The	semantic	model	contains	data	from	the	following	data
sources:
•Source1:	A	Microsoft	Excel	file	stored	in	Microsoft	OneDrive	for	Business
•Source2:	An	Azure	SQL	database	on	a	virtual	network
•Source3:	A	public	website
Which	data	sources	require	an	on-premises	data	gateway?
A.
Source1	only
B.
Source2	only
C.
Source3	only
D.
Source1	and	Source2	only
E.
Source2	and	Source3	only
F.
Source1,	Source2,	and	Source3
Answer:	
B
Explanation:
Correct	answer	is	B:Source2	only.
HOTSPOT
-
You	have	a	Power	BI	semantic	model	named	ModelA	that	contains	the	following	columns:

**Réponse exacte :**
You	have	a	Power	BI	semantic	model	that	contains	two	queries.
You	discover	that	a	report	based	on	the	model	has	performance	issues.
You	plan	to	use	Power	Query	to	reduce	the	data	loaded	to	the	model.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	answer	is	worth	one	point.
A.
Apply	group	by	and	summarize	techniques.
B.
Combine	the	queries	by	using	Append.
C.
Remove	unnecessary	columns	and	rows.
D.
Combine	the	queries	by	using	Merge.
E.
Create	a	new	query	group.
Answer:	
AC

**Explication courte :**
A.Apply	group	by	and	summarize	techniques.
C.Remove	unnecessary	columns	and	rows.
Reference:
https://learn.microsoft.com/en-us/power-bi/guidance/import-modeling-data-reduction
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	an	on-premises	data	gateway.
You	need	to	reduce	the	amount	of	data	sent	through	the	gateway	by	semantic	models	that	run	in	Import	storage

---

## Question 143
**Énoncé de la question :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	an	on-premises	data	gateway.
You	need	to	reduce	the	amount	of	data	sent	through	the	gateway	by	semantic	models	that	run	in	Import	storage

**Réponse exacte :**
B

**Explication courte :**
Create	aggregations	to	summarize	results.This	seems	to	be	saying	group	and	summarize	after	the	data	has
come	through	the	gateway	as	an	import.This	will	not	reduce	the	traffic	as	it	has	already	come	through	the
gateway.Answer	:	B.No.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	an	on-premises	data	gateway.
You	need	to	reduce	the	amount	of	data	sent	through	the	gateway	by	semantic	models	that	run	in	import	storage
mode.
Solution:	You	increase	Automatic	page	refresh	intervals.
Does	this	meet	the	goal?
A.
Yes
B.
No
Answer:	
B
Explanation:
1)	Nothing	to	do	with	On-Prem	data	gateway2)	It	can	be	used	with	DirectQuery	storage	mode	only.
https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-automatic-page-refresh
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	an	on-premises	data	gateway.

---

## Question 145
**Énoncé de la question :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	an	on-premises	data	gateway.

**Réponse exacte :**
A

**Explication courte :**
Correct	answer	is	A:Yes.
DRAG	DROP	-
You	have	a	Microsoft	Excel	spreadsheet	that	contains	the	data	shown	in	the	following	table.
You	plan	to	build	a	data	model	for	a	Power	BI	report.
You	need	to	prepare	the	data	so	that	it	is	available	to	the	model	in	the	format	shown	in	the	following	table.
Which	three	actions	should	you	perform	in	sequence	in	Power	Query	Editor?	To	answer,	move	the	appropriate
actions	from	the	list	of	actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:

---

## Question 146
**Énoncé de la question :**
Correct	answer	is	A:Yes.
DRAG	DROP	-
You	have	a	Microsoft	Excel	spreadsheet	that	contains	the	data	shown	in	the	following	table.
You	plan	to	build	a	data	model	for	a	Power	BI	report.
You	need	to	prepare	the	data	so	that	it	is	available	to	the	model	in	the	format	shown	in	the	following	table.
Which	three	actions	should	you	perform	in	sequence	in	Power	Query	Editor?	To	answer,	move	the	appropriate
actions	from	the	list	of	actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:

**Réponse exacte :**


**Explication courte :**
Step	1:	Select	the	[Department]	and	[Stage]	columns	and	unpivot	the	other	columns.
We	unpivot	the	School1,	School2,	School3,	and	the	School4	columns.
You	might	want	to	unpivot	data,	sometimes	called	flattening	the	data,	to	put	it	in	a	matrix	format	so	that	all
similar	values	are	in	one	column.
Example:
When	you	unpivot,	you	unpack	the	attribute-value	pairs	that	represent	an	intersection	point	of	the	new
columns	and	re-orient	them	into	flattened	columns:
*	Values	(in	blue	on	the	left)	are	unpivoted	into	a	new	column	(in	blue	on	the	right).
*	Attributes	(in	green	on	the	left)	are	unpivoted	into	a	new	column	(in	green	on	the	right)	and	duplicates	are
correspondingly	mapped	to	the	new	Values	column.
Step	2:	Rename	the	[Attribute]	column	as	[School]	and	the	[Value]	column	as	[Score[,
Step	3:	Group	by	[Department]	and	[School]	and..
Reference:
https://support.microsoft.com/en-us/office/unpivot-columns-power-query-0f7bad4b-9ea1-49c1-9d95-f5882
21c7098
You	have	a	report	that	contains	a	bar	chart	and	a	column	chart.	The	bar	chart	shows	customer	count	by	customer
segment.	The	column	chart	shows	sales	by	month.
You	need	to	ensure	that	when	a	segment	is	selected	in	the	bar	chart,	you	see	which	portion	of	the	total	sales	for
the	month	belongs	to	the	customer	segment.
How	should	the	visual	interactions	be	set	on	the	column	chart	when	the	bar	chart	is	selected?
A.	
highlight
B.	
filter
C.	
no	impact
Answer:	
A

---

## Question 147
**Énoncé de la question :**
21c7098
You	have	a	report	that	contains	a	bar	chart	and	a	column	chart.	The	bar	chart	shows	customer	count	by	customer
segment.	The	column	chart	shows	sales	by	month.
You	need	to	ensure	that	when	a	segment	is	selected	in	the	bar	chart,	you	see	which	portion	of	the	total	sales	for
the	month	belongs	to	the	customer	segment.
How	should	the	visual	interactions	be	set	on	the	column	chart	when	the	bar	chart	is	selected?
A.	
highlight
B.	
filter
C.	
no	impact
Answer:	
A

**Réponse exacte :**


**Explication courte :**
In	most	visuals,	highlighting	doesn't	remove	the	unrelated	data.	Instead	it	highlights	the	related	data.	The	rest
of	the	data	remains	visible	but	dimmed.
Note:	By	default,	visualizations	on	a	report	page	can	be	used	to	cross-filter	and	cross-highlight	the	other
visualizations	on	the	page.	For	example,	selecting	a	state	on	a	map	visualization	highlights	the	column	chart
and	filters	the	line	chart	to	display	only	data	that	applies	to	that	one	state.
Incorrect:
Not	B:	Filters	remove	all	but	the	data	you	want	to	focus	on.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-reports-filters-and-highlighting
A	user	creates	a	Power	BI	report	named	ReportA	that	uses	a	custom	theme.
You	create	a	dashboard	named	DashboardA.
You	need	to	ensure	that	DashboardA	uses	the	custom	theme.	The	solution	must	minimize	development	effort.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Publish	ReportA	to	Power	BI.
B.	
From	ReportA	save	the	current	theme.
C.	
Publish	ReportA	to	the	Microsoft	Power	BI	Community	theme	gallery.
D.	
From	DashboardA,	create	a	custom	theme.
E.	
From	DashboardA,	upload	a	JSON	theme.
Answer:	
BE
Explanation:
B.	From	ReportA	save	the	current	theme.
E.	From	DashboardA,	upload	a	JSON	theme.
​
https://learn.microsoft.com/en-us/power-bi/create-reports/service-dashboard-themes
scroll	down	to	part	that	says	JSON	themes
You	need	to	create	a	visualization	that	compares	revenue	and	cost	over	time.
Which	type	of	visualization	should	you	use?
A.	
waterfall	chart
B.	
stacked	area	chart
C.	
line	chart
D.	
donut	chart

---

## Question 149
**Énoncé de la question :**
A	user	creates	a	Power	BI	report	named	ReportA	that	uses	a	custom	theme.
You	create	a	dashboard	named	DashboardA.
You	need	to	ensure	that	DashboardA	uses	the	custom	theme.	The	solution	must	minimize	development	effort.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Publish	ReportA	to	Power	BI.
B.	
From	ReportA	save	the	current	theme.
C.	
Publish	ReportA	to	the	Microsoft	Power	BI	Community	theme	gallery.
D.	
From	DashboardA,	create	a	custom	theme.
E.	
From	DashboardA,	upload	a	JSON	theme.
Answer:	
BE
Explanation:
B.	From	ReportA	save	the	current	theme.
E.	From	DashboardA,	upload	a	JSON	theme.
​
https://learn.microsoft.com/en-us/power-bi/create-reports/service-dashboard-themes
scroll	down	to	part	that	says	JSON	themes
You	need	to	create	a	visualization	that	compares	revenue	and	cost	over	time.
Which	type	of	visualization	should	you	use?
A.	
waterfall	chart
B.	
stacked	area	chart
C.	
line	chart
D.	
donut	chart

**Réponse exacte :**
C

**Explication courte :**
Line	charts	can	have	many	different	lines,	for	example	both	revenue	and	cost	over	time.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-line-chart

---

## Question 150
**Énoncé de la question :**
HOTSPOT	-
You	have	a	report	in	Power	BI	Desktop.
You	add	a	key	influencers	visual	as	shown	in	the	exhibit.	(Click	the	Exhibit	tab.)
Use	the	drop-down	menus	to	select	the	answer	choice	that	completes	each	statement	based	on	the	information
presented	in	the	graphic.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:	adding	more	fields	to	Explain	By
Box	2:	3
0.30	instead	of	0.10.	A	factor	of	3	greater.
moving	fields	from	explain	to	expand	should	not	add	any	new	factors	in	analysis
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers
You	build	a	report	to	help	the	sales	team	understand	its	performance	and	the	drivers	of	sales.
The	team	needs	to	have	a	single	visualization	to	identify	which	factors	affect	success.
Which	type	of	visualization	should	you	use?
A.	
Key	influencers
B.	
Line	and	clustered	column	chart
C.	
Q&A
D.	
Funnel	chart
Answer:	
A
Explanation:
The	key	influencers	visual	helps	you	understand	the	factors	that	drive	a	metric	you're	interested	in.	It	analyzes
your	data,	ranks	the	factors	that	matter,	and	displays	them	as	key	influencers.	For	example,	suppose	you	want
to	figure	out	what	influences	employee	turnover,	which	is	also	known	as	churn.	One	factor	might	be
employment	contract	length,	and	another	factor	might	be	commute	time.
When	to	use	key	influencers.
The	key	influencers	visual	is	a	great	choice	if	you	want	to:
See	which	factors	affect	the	metric	being	analyzed.
Contrast	the	relative	importance	of	these	factors.	For	example,	do	short-term	contracts	affect	churn	more
than	long-term	contracts?

---

## Question 152
**Énoncé de la question :**
You	build	a	report	to	help	the	sales	team	understand	its	performance	and	the	drivers	of	sales.
The	team	needs	to	have	a	single	visualization	to	identify	which	factors	affect	success.
Which	type	of	visualization	should	you	use?
A.	
Key	influencers
B.	
Line	and	clustered	column	chart
C.	
Q&A
D.	
Funnel	chart
Answer:	
A
Explanation:
The	key	influencers	visual	helps	you	understand	the	factors	that	drive	a	metric	you're	interested	in.	It	analyzes
your	data,	ranks	the	factors	that	matter,	and	displays	them	as	key	influencers.	For	example,	suppose	you	want
to	figure	out	what	influences	employee	turnover,	which	is	also	known	as	churn.	One	factor	might	be
employment	contract	length,	and	another	factor	might	be	commute	time.
When	to	use	key	influencers.
The	key	influencers	visual	is	a	great	choice	if	you	want	to:
See	which	factors	affect	the	metric	being	analyzed.
Contrast	the	relative	importance	of	these	factors.	For	example,	do	short-term	contracts	affect	churn	more
than	long-term	contracts?

**Réponse exacte :**


**Explication courte :**
Box	1:	
Total	Sales	-
The	key	influencers	visual	helps	you	understand	the	factors	that	drive	a	metric	you're	interested	in,	here	Total
Sales.	It	analyses	your	data,	ranks	the	factors	that	matter,	and	displays	them	as	key	influencers.
Box	2:	
Occupation	-
Measures	and	summarized	columns	are	automatically	analysed	at	the	level	of	the	Explain	by	fields	used.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers
You	are	using	the	key	influencers	visual	to	identify	which	factors	affect	the	quantity	of	items	sold	in	an	order.
You	add	the	following	fields	to	the	Explain	By	field:
✑
	Customer	Country
✑
	Product	Category
✑
	Supplier	Country
✑
	Sales	Employee
✑
	Supplier	Name
✑
	Product	Name
✑
	Customer	City
The	key	influencers	visual	returns	the	results	shown	in	the	following	exhibit.

---

## Question 153
**Énoncé de la question :**
You	are	using	the	key	influencers	visual	to	identify	which	factors	affect	the	quantity	of	items	sold	in	an	order.
You	add	the	following	fields	to	the	Explain	By	field:
✑
	Customer	Country
✑
	Product	Category
✑
	Supplier	Country
✑
	Sales	Employee
✑
	Supplier	Name
✑
	Product	Name
✑
	Customer	City
The	key	influencers	visual	returns	the	results	shown	in	the	following	exhibit.

**Réponse exacte :**
A

**Explication courte :**
Average	quantity	of	units	is	displayed.
Incorrect:
Not	B:	Average	quantity	of	units	is	displayed,	not	percentage.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers
You	have	a	report	that	contains	four	pages.	Each	page	contains	slicers	for	the	same	four	fields.
Users	report	that	when	they	select	values	in	a	slicer	on	one	page,	the	selections	are	not	persisted	on	other	pages.
You	need	to	recommend	a	solution	to	ensure	that	users	can	select	a	value	once	to	filter	the	results	on	all	the
pages.
What	are	two	possible	recommendations	to	achieve	this	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

---

## Question 154
**Énoncé de la question :**
You	have	a	report	that	contains	four	pages.	Each	page	contains	slicers	for	the	same	four	fields.
Users	report	that	when	they	select	values	in	a	slicer	on	one	page,	the	selections	are	not	persisted	on	other	pages.
You	need	to	recommend	a	solution	to	ensure	that	users	can	select	a	value	once	to	filter	the	results	on	all	the
pages.
What	are	two	possible	recommendations	to	achieve	this	goal?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**
BC

**Explication courte :**
C:	You	can	sync	a	slicer	and	use	it	on	any	or	all	pages	in	a	report.
B:	You	can	set	filters	at	three	different	levels	for	the	report:	visual-level,	page-level,	and	report-level.
Note:	Suppose	you	want	your	report	readers	to	be	able	to	look	at	overall	sales	metrics,	but	also	highlight
performance	for	individual	district	managers	and	different	time	frames.	You	could	create	separate	reports	or
comparative	charts.	You	could	add	filters	in	the	Filters	pane.	Or	you	could	use	slicers.	Slicers	are	another	way
of	filtering.	They	narrow	the	portion	of	the	dataset	that	is	shown	in	the	other	report	visualizations.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-report-add-filter
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers
You	have	a	report	that	includes	a	card	visualization.
You	need	to	apply	the	following	conditional	formatting	to	the	card	while	minimizing	design	effort:
✑
	For	values	that	are	greater	than	or	equal	to	100,	the	font	of	the	data	label	must	be	dark	red.
✑
	For	values	that	are	less	than	100,	the	font	of	the	data	label	must	be	dark	gray.
Which	type	of	format	should	you	use?
A.	
Color	scale
B.	
Rules
C.	
Field	value
Answer:	
B
Explanation:
Finding	the	conditional	formatting	in	the	card	visual	is	a	bit	tricky.	There	is	no	separate	option	for	that.	You
need	to	go	to	the	Format	tab	of	the	visual,	and	then	expand	the	Data	Label.	The	right	beside	the	Data	Label's
colour	you	need	to	hover	your	mouse,	and	you	will	find	a	three	dots	icon	appearing,	which	if	you	click	on	it,	you
will	see	Conditional	Formatting.

---

## Question 155
**Énoncé de la question :**
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers
You	have	a	report	that	includes	a	card	visualization.
You	need	to	apply	the	following	conditional	formatting	to	the	card	while	minimizing	design	effort:
✑
	For	values	that	are	greater	than	or	equal	to	100,	the	font	of	the	data	label	must	be	dark	red.
✑
	For	values	that	are	less	than	100,	the	font	of	the	data	label	must	be	dark	gray.
Which	type	of	format	should	you	use?
A.	
Color	scale
B.	
Rules
C.	
Field	value
Answer:	
B
Explanation:
Finding	the	conditional	formatting	in	the	card	visual	is	a	bit	tricky.	There	is	no	separate	option	for	that.	You
need	to	go	to	the	Format	tab	of	the	visual,	and	then	expand	the	Data	Label.	The	right	beside	the	Data	Label's
colour	you	need	to	hover	your	mouse,	and	you	will	find	a	three	dots	icon	appearing,	which	if	you	click	on	it,	you
will	see	Conditional	Formatting.

**Réponse exacte :**


**Explication courte :**
3>2>1
1.	From	DashboardA,	select	the	TilaA	options,	and	then	select	View	Insights
2.	From	Focus	mode,	review	the	generated	visuals
3.From	Focus	mode,	pin	the	relevant	visuals	to	DashboardA
Source:	https://learn.microsoft.com/en-us/power-bi/consumer/end-user-insights

---

## Question 157
**Énoncé de la question :**
3>2>1
1.	From	DashboardA,	select	the	TilaA	options,	and	then	select	View	Insights
2.	From	Focus	mode,	review	the	generated	visuals
3.From	Focus	mode,	pin	the	relevant	visuals	to	DashboardA
Source:	https://learn.microsoft.com/en-us/power-bi/consumer/end-user-insights

**Réponse exacte :**
D

**Explication courte :**
One	way	to	add	a	new	dashboard	tile	is	by	pinning	an	entire	report	page.	This	is	an	easy	way	to	pin	more	than
one	visualization	at	a	time.	Also,	when	you	pin	an	entire	page,	the	tiles	are	live;	you	can	interact	with	them
right	there	on	the	dashboard.	And	changes	you	make	to	any	of	the	visualizations	back	in	the	report	editor,	like
adding	a	filter	or	changing	the	fields	used	in	the	chart,	are	reflected	in	the	dashboard	tile	as	well.
Pinning	live	tiles	from	reports	to	dashboards	is	only	available	in	Power	BI	service	(app.powerbi.com).
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-pin-live-tile-from-report

---

## Question 158
**Énoncé de la question :**
HOTSPOT	-
You	need	to	create	a	visual	as	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Box	1:	Background	color	-
To	apply	conditional	formatting,	select	a	Table	or	Matrix	visualization	in	Power	BI	Desktop.	In	the
Visualizations	pane,	right-click	or	select	the	down-arrow	next	to	the	field	in	the	Values	well	that	you	want	to
format.	Select	Conditional	formatting,	and	then	select	the	type	of	formatting	to	apply.
Box	2:	Rules	-
To	format	cell	background	or	font	color	by	rules,	in	the	Format	by	field	of	the	Background	color	or	Font	color
dialog	box,	select	Rules.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-conditional-table-formatting
DRAG	DROP	-
You	are	using	existing	reports	to	build	a	dashboard	that	will	be	viewed	frequently	in	portrait	mode	on	mobile
phones.
You	need	to	build	the	dashboard.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
Pin	->	open	->	edit	->	rearrange
Step	1:	Pin	items	from	the	reports	to	the	dashboard
Step	2:	Open	the	dashboard.
Open	the	dashboard	to	see	the	pinned	live	tile,
From	the	nav	pane,	select	the	dashboard	with	the	new	live	tile.	There,	you	can	do	things	like	rename,	resize,
link,	and	move	the	pinned	report	page.
Step	3:	Edit	the	dashboard	mobile	view

---

## Question 159
**Énoncé de la question :**
DRAG	DROP	-
You	are	using	existing	reports	to	build	a	dashboard	that	will	be	viewed	frequently	in	portrait	mode	on	mobile
phones.
You	need	to	build	the	dashboard.
Which	four	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
Pin	->	open	->	edit	->	rearrange
Step	1:	Pin	items	from	the	reports	to	the	dashboard
Step	2:	Open	the	dashboard.
Open	the	dashboard	to	see	the	pinned	live	tile,
From	the	nav	pane,	select	the	dashboard	with	the	new	live	tile.	There,	you	can	do	things	like	rename,	resize,
link,	and	move	the	pinned	report	page.
Step	3:	Edit	the	dashboard	mobile	view

**Réponse exacte :**
C

**Explication courte :**
The	analytics	feature	enables	you	to	show	percentiles	across	groups	specified	along	a	specific	axis.
1.	Click	on	the	analytics	tab
2.	Select	Percentile
3.	You	can	choose	a	specific	percentile	along	with	other	formatting	options.
4.	Drag	a	date	or	non-numeric	dimension	into	the	Axis	of	a	column	chart

---

## Question 160
**Énoncé de la question :**
The	analytics	feature	enables	you	to	show	percentiles	across	groups	specified	along	a	specific	axis.
1.	Click	on	the	analytics	tab
2.	Select	Percentile
3.	You	can	choose	a	specific	percentile	along	with	other	formatting	options.
4.	Drag	a	date	or	non-numeric	dimension	into	the	Axis	of	a	column	chart

**Réponse exacte :**
BD

**Explication courte :**


---

## Question 162
**Énoncé de la question :**


**Réponse exacte :**
B

**Explication courte :**
Filters	remove	all	but	the	data	you	want	to	focus	on.
Note:	Enable	the	visual	interaction	controls.
1.	Select	a	visualization	to	make	it	active.
2.	Display	the	Visual	Interactions	options.
3.	In	Power	BI	Desktop,	select	Format	>	Edit	interactions.
4.	To	display	the	visualization	interaction	controls,	select	Edit	interactions.	Power	BI	adds	filter	and	highlight
icons	to	all	of	the	other	visualizations	on	the	report	page.
We	can	see	that	the	tree	map	is	cross-filtering	the	line	chart	and	the	map,	and	is	cross-highlighting	the
column	chart.	You	can	now	change	how	the	selected	visualization	interacts	with	the	other	visualizations	on	the
report	page.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions

---

## Question 163
**Énoncé de la question :**
HOTSPOT	-
You	have	a	report	page	that	contains	the	visuals	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Box	1:	not	affect
Box	2:	cross-filter	-
The	map	has	the	cross-filter	icon	active.
"You	can	only	cross-filter	line	charts,	scatter	charts,	and	maps.	You	can't	cross-highlight	them"	So	Cross-filter
for	the	map
https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions?tabs=powerbi-
desktop
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions
You	are	creating	a	Power	BI	report	by	using	Power	BI	Desktop.
You	need	to	include	a	visual	that	shows	trends	and	other	useful	information	automatically.	The	visual	must	update
based	on	selections	in	other	visuals.
Which	type	of	visual	should	you	use?
A.	
Q&A
B.	
smart	narrative
C.	
key	influencers
D.	
decomposition	tree
Answer:	
B
Explanation:
The	smart	narrative	visualization	helps	you	quickly	summarize	visuals	and	reports.	It	provides	relevant
innovative	insights	that	you	can	customize.
Use	smart	narrative	summaries	in	your	reports	to	address	key	takeaways,	to	point	out	trends,	and	to	edit	the
language	and	format	for	a	specific	audience.	In
PowerPoint,	instead	of	pasting	a	screenshot	of	your	report's	key	takeaways,	you	can	add	narratives	that	are
updated	with	every	refresh.	Your	audience	can	use	the	summaries	to	understand	the	data,	get	to	key	points
faster,	and	explain	the	data	to	others.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-smart-narrative
In	Power	BI	Desktop,	you	have	a	dataset	that	contains	a	table.
You	create	a	table	visual	on	a	Power	BI	report	page	as	shown	in	the	following	exhibit.
You	need	to	configure	the	visual	to	display	the	referenced	image	instead	of	the	URL	in	the	Plant	Image	column.
What	should	you	do?
A.	
From	the	Formatting	tab,	select	Values,	and	then	set	URL	icons	to	On	for	the	table.

---

## Question 165
**Énoncé de la question :**
desktop
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions
You	are	creating	a	Power	BI	report	by	using	Power	BI	Desktop.
You	need	to	include	a	visual	that	shows	trends	and	other	useful	information	automatically.	The	visual	must	update
based	on	selections	in	other	visuals.
Which	type	of	visual	should	you	use?
A.	
Q&A
B.	
smart	narrative
C.	
key	influencers
D.	
decomposition	tree
Answer:	
B
Explanation:
The	smart	narrative	visualization	helps	you	quickly	summarize	visuals	and	reports.	It	provides	relevant
innovative	insights	that	you	can	customize.
Use	smart	narrative	summaries	in	your	reports	to	address	key	takeaways,	to	point	out	trends,	and	to	edit	the
language	and	format	for	a	specific	audience.	In
PowerPoint,	instead	of	pasting	a	screenshot	of	your	report's	key	takeaways,	you	can	add	narratives	that	are
updated	with	every	refresh.	Your	audience	can	use	the	summaries	to	understand	the	data,	get	to	key	points
faster,	and	explain	the	data	to	others.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-smart-narrative
In	Power	BI	Desktop,	you	have	a	dataset	that	contains	a	table.
You	create	a	table	visual	on	a	Power	BI	report	page	as	shown	in	the	following	exhibit.
You	need	to	configure	the	visual	to	display	the	referenced	image	instead	of	the	URL	in	the	Plant	Image	column.
What	should	you	do?
A.	
From	the	Formatting	tab,	select	Values,	and	then	set	URL	icons	to	On	for	the	table.

**Réponse exacte :**
D

**Explication courte :**
Add	images	to	your	report	-
1.	Create	a	column	with	the	URLs	of	the	images.	See	Considerations	later	in	this	article	for	requirements.
2.	Select	that	column.	On	the	Column	tools	ribbon,	for	Data	category,	select	Image	URL.
3.	Add	the	column	to	a	table,	matrix,	slicer,	or	multi-row	card.
Step	3:	From	powerbi.com,	add	a	tile	for	Excel1	dataset	to	DashboardA.
In	the	Power	BI	service	(app.powerbi.com),	a	dashboard	contains	tiles	pinned	from	one	or	more	datasets,	so
you	can	ask	questions	about	any	of	the	data	contained	in	any	of	those	datasets.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-images-tables	https://docs.microsoft.co
m/en-us/power-bi/create-reports/power-bi-tutorial-q-and-a
DRAG	DROP	-
You	have	a	Microsoft	Excel	spreadsheet	named	Excel1	that	contains	survey	results.
You	have	a	Power	BI	dashboard	named	DashboardA	that	has	Q&A	enabled.
You	need	to	ensure	that	users	who	can	access	DashboardA	can	ask	questions	based	on	the	contents	of	Excel1	and
pin	visuals	based	on	their	queries	to
DashboardA.	The	solution	must	minimize	development	time.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
Step	1:	["The	solution	must	minimize	development	time",	so:]	
format	the	data	as	a	table
Step	2:	
From	powerbi.com,	import	Excel1	as	a	dataset.
Step	3:	
From	powerbi.com,	add	a	tile	for	the	Excel1	dataset	to	DashboarA.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-from-excel-to-stunning-report

---

## Question 166
**Énoncé de la question :**
https://docs.microsoft.co
m/en-us/power-bi/create-reports/power-bi-tutorial-q-and-a
DRAG	DROP	-
You	have	a	Microsoft	Excel	spreadsheet	named	Excel1	that	contains	survey	results.
You	have	a	Power	BI	dashboard	named	DashboardA	that	has	Q&A	enabled.
You	need	to	ensure	that	users	who	can	access	DashboardA	can	ask	questions	based	on	the	contents	of	Excel1	and
pin	visuals	based	on	their	queries	to
DashboardA.	The	solution	must	minimize	development	time.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:
Answer:
Explanation:
Step	1:	["The	solution	must	minimize	development	time",	so:]	
format	the	data	as	a	table
Step	2:	
From	powerbi.com,	import	Excel1	as	a	dataset.
Step	3:	
From	powerbi.com,	add	a	tile	for	the	Excel1	dataset	to	DashboarA.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-from-excel-to-stunning-report

**Réponse exacte :**
B

**Explication courte :**
Instead:	You	create	a	percentile	line	by	using	the	Salary	measure	and	set	the	percentile	to	50%.
The	median	is	the	middle	value	or	the	50th	percentile	of	a	data	set.
Reference:
https://dash-intel.com/powerbi/statistical_functions_median.php
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	clustered	bar	chart	that	contains	a	measure	named	Salary	as	the	value	and	a	field	named	Employee	as
the	axis.	Salary	is	present	in	the	data	as	a	numerical	amount	representing	US	dollars.
You	need	to	create	a	reference	line	to	show	which	employees	are	above	the	median	salary.
Solution:	You	create	an	average	line	by	using	the	Salary	measure.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Average	is	not	Median.
Instead:	You	create	a	percentile	line	by	using	the	Salary	measure	and	set	the	percentile	to	50%.
The	median	is	the	middle	value	or	the	50th	percentile	of	a	data	set.
Reference:
https://dash-intel.com/powerbi/statistical_functions_median.php
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.

---

## Question 169
**Énoncé de la question :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	clustered	bar	chart	that	contains	a	measure	named	Salary	as	the	value	and	a	field	named	Employee	as
the	axis.	Salary	is	present	in	the	data	as	a	numerical	amount	representing	US	dollars.
You	need	to	create	a	reference	line	to	show	which	employees	are	above	the	median	salary.
Solution:	You	create	an	average	line	by	using	the	Salary	measure.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
Average	is	not	Median.
Instead:	You	create	a	percentile	line	by	using	the	Salary	measure	and	set	the	percentile	to	50%.
The	median	is	the	middle	value	or	the	50th	percentile	of	a	data	set.
Reference:
https://dash-intel.com/powerbi/statistical_functions_median.php
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.

**Réponse exacte :**
A

**Explication courte :**
The	median	is	the	middle	value	or	the	50th	percentile	of	a	data	set.
Reference:
https://dash-intel.com/powerbi/statistical_functions_median.php

---

## Question 170
**Énoncé de la question :**
HOTSPOT	-
You	are	profiling	data	by	using	Power	Query	Editor.
You	have	a	table	that	contains	a	column	named	column1.	Column	statistics	and	Value	distribution	for	column1	are
shown	in	the	following	exhibit.
Use	the	drop-down	menus	to	select	the	answer	choice	that	completes	each	statement	based	on	the	information
presented	in	the	graphic.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
Box	1:
	are	20	values	that	occur	-
There	are	20	unique	values.
Box	2:	
Elm,	American	-
Elm,	American	is	below	Peer,	flowering	species	in	the	graphic.
“Distinct”	means	number	of	different	values	regardless	how	many	times	it	appears	in	the	dataset.	A	'name'
appears	in	the	list	multiple	times	is	counted	as	1	distinct	count.
Whereas,	the	“Unique”	value	is	total	number	of	values	that	only	appear	once.	
Distinct	mean	:	count	all	the	values	as	1,	even	if	there	was	more	than	one.
Unique	mean	:	count	only	the	value	that	are	not	repeated	in	the	particular	column
You	have	a	Power	BI	report	hosted	on	powerbi.com	that	displays	expenses	by	department	for	department
managers.
The	report	contains	a	line	chart	that	shows	expenses	by	month.
You	need	to	enable	users	to	choose	between	viewing	the	report	as	a	line	chart	or	a	column	chart.	The	solution	must
minimize	development	and	maintenance	effort.
What	should	you	do?
A.	
Enable	report	readers	to	personalize	visuals.
B.	
Create	a	separate	report	page	for	users	to	view	the	column	chart.
C.	
Add	a	column	chart,	a	bookmark,	and	a	button	for	users	to	choose	a	visual.
D.	
Create	a	mobile	report	that	contains	a	column	chart.
Answer:	
A
Explanation:
Also	C	is	correct	but	I	guess	the	key	is	'The	solution	must	minimize	development'	so	A	should	be	the	correct
one
Steps:
Let	users	personalize	visuals	in	a	report
Enable	personalization	in	a	report
You	can	enable	the	feature	either	in	Power	BI	Desktop	or	the	Power	BI	service.	You	can	also	enable	it	in
embedded	reports.
To	enable	the	feature	in	the	Power	BI	(powerbi.com)	service,	go	to	Settings	for	your	report.

---

## Question 172
**Énoncé de la question :**
Box	1:
	are	20	values	that	occur	-
There	are	20	unique	values.
Box	2:	
Elm,	American	-
Elm,	American	is	below	Peer,	flowering	species	in	the	graphic.
“Distinct”	means	number	of	different	values	regardless	how	many	times	it	appears	in	the	dataset.	A	'name'
appears	in	the	list	multiple	times	is	counted	as	1	distinct	count.
Whereas,	the	“Unique”	value	is	total	number	of	values	that	only	appear	once.	
Distinct	mean	:	count	all	the	values	as	1,	even	if	there	was	more	than	one.
Unique	mean	:	count	only	the	value	that	are	not	repeated	in	the	particular	column
You	have	a	Power	BI	report	hosted	on	powerbi.com	that	displays	expenses	by	department	for	department
managers.
The	report	contains	a	line	chart	that	shows	expenses	by	month.
You	need	to	enable	users	to	choose	between	viewing	the	report	as	a	line	chart	or	a	column	chart.	The	solution	must
minimize	development	and	maintenance	effort.
What	should	you	do?
A.	
Enable	report	readers	to	personalize	visuals.
B.	
Create	a	separate	report	page	for	users	to	view	the	column	chart.
C.	
Add	a	column	chart,	a	bookmark,	and	a	button	for	users	to	choose	a	visual.
D.	
Create	a	mobile	report	that	contains	a	column	chart.
Answer:	
A
Explanation:
Also	C	is	correct	but	I	guess	the	key	is	'The	solution	must	minimize	development'	so	A	should	be	the	correct
one
Steps:
Let	users	personalize	visuals	in	a	report
Enable	personalization	in	a	report
You	can	enable	the	feature	either	in	Power	BI	Desktop	or	the	Power	BI	service.	You	can	also	enable	it	in
embedded	reports.
To	enable	the	feature	in	the	Power	BI	(powerbi.com)	service,	go	to	Settings	for	your	report.

**Réponse exacte :**
CD

**Explication courte :**
D:	With	dashboard	themes	you	can	apply	a	color	theme	to	your	entire	dashboard,	such	as	corporate	colors,
seasonal	coloring,	or	any	other	color	theme	you	might	want	to	apply.	When	you	apply	a	dashboard	theme,	all
visuals	on	your	dashboard	use	the	colors	from	your	selected	theme.
In	the	dashboard	pane	that	appears,	select	one	of	the	pre-built	themes.	In	the	example	below,	we've	selected
Dark.
C:	Reports	and	dashboards	with	different	themes
If	your	report	uses	a	different	theme	from	the	dashboard	theme,	in	most	cases	you	can	control	whether	the
visual	retains	the	current	report	theme	or	uses	the	dashboard	theme.
*	Try	re-pinning	the	tile	and	selecting	Use	dashboard	theme.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-themes

---

## Question 173
**Énoncé de la question :**
HOTSPOT	-
You	have	a	dataset	that	contains	revenue	data	from	the	past	year.
You	need	to	use	anomaly	detection	in	Power	BI	to	show	anomalies	in	the	dataset.
What	should	you	configure?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:

**Réponse exacte :**


**Explication courte :**
Box	1:	
Line	-
Anomaly	detection	is	only	supported	for	line	chart	visuals	containing	time	series	data	in	the	Axis	field.
Box	2:	
Populate	the	axis	with	a	date	field
Incorrect:
*	Anomaly	Explanations	doesn't	work	with	'Show	Value	As'	options.
*	Drilling	down	to	go	to	the	next	level	in	the	hierarchy	isn't	supported.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-anomaly-detection
You	have	a	line	chart	that	shows	the	number	of	employees	in	a	department	over	time.
You	need	to	see	the	total	salary	costs	of	the	employees	when	you	hover	over	a	data	point.
What	should	you	do?
A.	
Add	salary	to	the	drillthrough	fields.
B.	
Add	salary	to	the	visual	filters.
C.	
Add	salary	to	the	tooltips.
Answer:	
C
Explanation:
Customize	tooltips	with	aggregation	or	quick	measures
You	can	customize	a	tooltip	by	selecting	an	aggregation	function.
Select	the	arrow	beside	the	field	in	the	Tooltips	bucket.	Then,	select	from	the	available	options.

---

## Question 175
**Énoncé de la question :**
You	have	a	line	chart	that	shows	the	number	of	employees	in	a	department	over	time.
You	need	to	see	the	total	salary	costs	of	the	employees	when	you	hover	over	a	data	point.
What	should	you	do?
A.	
Add	salary	to	the	drillthrough	fields.
B.	
Add	salary	to	the	visual	filters.
C.	
Add	salary	to	the	tooltips.
Answer:	
C
Explanation:
Customize	tooltips	with	aggregation	or	quick	measures
You	can	customize	a	tooltip	by	selecting	an	aggregation	function.
Select	the	arrow	beside	the	field	in	the	Tooltips	bucket.	Then,	select	from	the	available	options.

**Réponse exacte :**
D

**Explication courte :**
For	example,	here's	how	the	current	forecast	looks	like:
Reference:
https://spreadsheeto.com/power-bi-forecasting/#intro
You	need	to	create	a	visual	that	enables	the	adhoc	exploration	of	data	as	shown	in	the	following	exhibit.

---

## Question 176
**Énoncé de la question :**
You	need	to	create	a	visual	that	enables	the	adhoc	exploration	of	data	as	shown	in	the	following	exhibit.

**Réponse exacte :**
B

**Explication courte :**
The	decomposition	tree	visual	in	Power	BI	lets	you	visualize	data	across	multiple	dimensions.	It	automatically
aggregates	data	and	enables	drilling	down	into	your	dimensions	in	any	order.	It	is	also	an	artificial	intelligence
(AI)	visualization,	so	you	can	ask	it	to	find	the	next	dimension	to	drill	down	into	based	on	certain	criteria.
This	makes	it	a	valuable	tool	for	ad	hoc	exploration	and	conducting	root	cause	analysis.
Example:
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-decomposition-tree
Your	company	has	employees	in	10	states.
The	company	recently	decided	to	associate	each	state	to	one	of	the	following	three	regions:	East,	West,	and	North.
You	have	a	data	model	that	contains	employee	information	by	state.	The	model	does	NOT	include	region
information.
You	have	a	report	that	shows	the	employees	by	state.
You	need	to	view	the	employees	by	region	as	quickly	as	possible.
What	should	you	do?
A.	
Create	a	new	aggregation	that	summarizes	by	state.
B.	
Create	a	new	aggregation	that	summarizes	by	employee.
C.	
Create	a	new	group	on	the	state	column	and	set	the	Group	type	to	List.
D.	
Create	a	new	group	on	the	state	column	and	set	the	Group	type	to	Bin.
Answer:	
C
Explanation:
In	Power	BI	Desktop,	you	can	group	data	points	to	help	you	more	clearly	view,	analyze,	and	explore	data	and
trends	in	your	visuals.
Example:

---

## Question 177
**Énoncé de la question :**
Your	company	has	employees	in	10	states.
The	company	recently	decided	to	associate	each	state	to	one	of	the	following	three	regions:	East,	West,	and	North.
You	have	a	data	model	that	contains	employee	information	by	state.	The	model	does	NOT	include	region
information.
You	have	a	report	that	shows	the	employees	by	state.
You	need	to	view	the	employees	by	region	as	quickly	as	possible.
What	should	you	do?
A.	
Create	a	new	aggregation	that	summarizes	by	state.
B.	
Create	a	new	aggregation	that	summarizes	by	employee.
C.	
Create	a	new	group	on	the	state	column	and	set	the	Group	type	to	List.
D.	
Create	a	new	group	on	the	state	column	and	set	the	Group	type	to	Bin.
Answer:	
C
Explanation:
In	Power	BI	Desktop,	you	can	group	data	points	to	help	you	more	clearly	view,	analyze,	and	explore	data	and
trends	in	your	visuals.
Example:

**Réponse exacte :**
C

**Explication courte :**
The	best	data	for	forecasting	is	time	series	data	or	uniformly	increasing	whole	numbers.	The	line	chart	has	to
have	only	one	line.
Reference:
https://powerbi.microsoft.com/fr-ca/blog/introducing-new-forecasting-capabilities-in-power-view-for-office-
365/

---

## Question 179
**Énoncé de la question :**
365/

**Réponse exacte :**
B

**Explication courte :**
A	tile	is	a	report	visual	pinned	to	a	dashboard,	and	dashboard	tile	refreshes	happen	about	every	hour	so	that
the	tiles	show	recent	results.	You	can	change	the	schedule	in	the	dataset	settings,	as	in	the	screenshot	below,
or	force	a	dashboard	update	manually	by	using	the	Refresh	now	option.
If	you	press	F5	or	hit	the	refresh	button,	the	dashboard	charts	gets	updated.
Note:	Power	BI	enables	you	to	go	from	data	to	insight	to	action	quickly,	yet	you	must	make	sure	the	data	in
your	Power	BI	reports	and	dashboards	is	recent.
Knowing	how	to	refresh	the	data	is	often	critical	in	delivering	accurate	results.
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/refresh-data

---

## Question 180
**Énoncé de la question :**
HOTSPOT	-
You	need	to	create	a	Power	BI	report.	The	first	page	of	the	report	must	contain	the	following	two	views:
✑
	Sales	By	Postal	Code
✑
	Sales	by	Month
Both	views	must	display	a	slicer	to	select	a	value	for	a	field	named	Chain.
The	Sales	By	Postal	Code	view	must	display	a	map	visual	as	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
Box	1:	2	-
One	for	each	visual.
Note:	When	you	edit	a	report	in	Power	BI	Desktop	and	the	Power	BI	service,	you	can	add	report	bookmarks	to
capture	the	current	state	of	a	report	page.
Bookmarks	save	the	current	filters	and	slicers,	cross-highlighted	visuals,	sort	order,	and	so	on.	When	others
view	your	report,	they	can	get	back	to	that	exact	state	by	selecting	your	saved	bookmark.
Box	2:	Display	-
Users	must	be	able	to	switch	between	the	views	by	using	buttons	on	the	report	page.	The	selected	Chain	field
must	be	maintained	when	switching	between	views.
You	can	select	whether	each	bookmark	will	apply	Data	properties,	such	as	filters	and	slicers;	Display
properties,	such	as	spotlight	and	its	visibility;	and	Current	page	changes,	which	present	the	page	that	was
visible	when	the	bookmark	was	added.	These	capabilities	are	useful	when	you	use	bookmarks	to	switch
between	report	views	or	selections	of	visuals,	in	which	case	you'd	likely	want	to	turn	off	data	properties,	so
that	filters	aren't	reset	when	users	switch	views	by	selecting	a	bookmark.
Note:	When	you	create	a	bookmark,	the	following	elements	are	saved	with	the	bookmark:
The	current	page	-
Filters	-
Slicers,	including	slicer	type	(for	example,	dropdown	or	list)	and	slicer	state
Visual	selection	state	(such	as	cross-highlight	filters)
Sort	order	-
Drill	location	-
Visibility	of	an	object	(by	using	the	Selection	pane)
The	focus	or	Spotlight	mode	of	any	visible	object
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-bookmarks
You	have	the	visual	shown	in	the	exhibit.	(Click	the	Exhibit	tab.)
You	need	to	show	the	relationship	between	Total	Cost	and	Total	Sales	over	time.
What	should	you	do?
A.	
Add	a	play	axis.
B.	
From	the	Analytics	pane,	add	an	Average	line.
C.	
Add	a	slicer	for	the	year.
D.	
Create	a	DAX	measure	that	calculates	year-over-year	growth.
Answer:	
A
Explanation:
When	to	use	a	slicer	-
Slicers	are	a	great	choice	when	you	want	to:
Display	commonly	used	or	important	filters	on	the	report	canvas	for	easier	access.
Make	it	easier	to	see	the	current	filtered	state	without	having	to	open	a	drop-down	list.
Filter	by	columns	that	are	unneeded	and	hidden	in	the	data	tables.
Create	more	focused	reports	by	putting	slicers	next	to	important	visuals.

---

## Question 182
**Énoncé de la question :**
You	have	the	visual	shown	in	the	exhibit.	(Click	the	Exhibit	tab.)
You	need	to	show	the	relationship	between	Total	Cost	and	Total	Sales	over	time.
What	should	you	do?
A.	
Add	a	play	axis.
B.	
From	the	Analytics	pane,	add	an	Average	line.
C.	
Add	a	slicer	for	the	year.
D.	
Create	a	DAX	measure	that	calculates	year-over-year	growth.
Answer:	
A
Explanation:
When	to	use	a	slicer	-
Slicers	are	a	great	choice	when	you	want	to:
Display	commonly	used	or	important	filters	on	the	report	canvas	for	easier	access.
Make	it	easier	to	see	the	current	filtered	state	without	having	to	open	a	drop-down	list.
Filter	by	columns	that	are	unneeded	and	hidden	in	the	data	tables.
Create	more	focused	reports	by	putting	slicers	next	to	important	visuals.

**Réponse exacte :**


**Explication courte :**
Box	1:
	Update	Dashboard	Mobile	Layout
Box	2:	
Resize	and	move	total	sales	and	total	quantity
Dashboard	mobile	feature	already	fits	the	tiles	in	the	view,	and	when	recreating	same	scenario	you	only	need
to	work	on	the	2	cards
If	you	use	Report	Mobile	View	feature	from	Power	BI	desktop,	you	will	have	an	empty	canvas	and	will	need	to
work	on	all	tiles
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-create-mobile-optimized-report-about
You	are	building	a	Power	BI	report	to	analyze	customer	segments.
You	need	to	identify	customer	segments	dynamically	based	on	the	Bounce	Rate	across	dimensions	such	as	source,
geography,	and	demographics.	The	solution	must	minimize	analysis	effort.
Which	type	of	visualization	should	you	use?
A.	
decomposition	tree
B.	
funnel	chart
C.	
Q&A
D.	
key	influencers
Answer:	
A

---

## Question 183
**Énoncé de la question :**
You	are	building	a	Power	BI	report	to	analyze	customer	segments.
You	need	to	identify	customer	segments	dynamically	based	on	the	Bounce	Rate	across	dimensions	such	as	source,
geography,	and	demographics.	The	solution	must	minimize	analysis	effort.
Which	type	of	visualization	should	you	use?
A.	
decomposition	tree
B.	
funnel	chart
C.	
Q&A
D.	
key	influencers
Answer:	
A

**Réponse exacte :**


**Explication courte :**
The	decomposition	tree	visual	in	Power	BI	lets	you	visualize	data	across	multiple	dimensions.	It	automatically
aggregates	data	and	enables	drilling	down	into	your	dimensions	in	any	order.	It	is	also	an	artificial	intelligence
(AI)	visualization,	so	you	can	ask	it	to	find	the	next	dimension	to	drill	down	into	based	on	certain	criteria.
This	makes	it	a	valuable	tool	for	ad	hoc	exploration	and	conducting	root	cause	analysis.
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-decomposition-tree
You	have	a	table	that	contains	sales	data	and	approximately	1,000	rows.
You	need	to	identify	outliers	in	the	table.
Which	type	of	visualization	should	you	use?
A.	
area	chart
B.	
scatter	plot
C.	
pie	chart
D.	
donut	chart
Answer:	
B
Explanation:
Outlier	Detection	in	Power	BI	using	Funnel	Plot,	which	is	a	scatter	plot.
Outliers	are	those	data	points	that	lie	outside	the	overall	pattern	of	distribution	&	the	easiest	way	to	detect
outliers	is	though	graphs.	Box	plots,	Scatter	plots	can	help	detect	them	easily.
Reference:
https://towardsdatascience.com/this-article-is-about-identifying-outliers-through-funnel-plots-using-the-mic
rosoft-power-bi-d7ad16ac9ccc
You	have	a	report	that	contains	three	pages.	One	of	the	pages	contains	a	KPI	visualization.
You	need	to	filter	all	the	visualizations	in	the	report	except	for	the	KPI	visualization.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Edit	the	interactions	of	the	KPI	visualization.
B.	
Add	the	same	slicer	to	each	page	and	configure	Sync	slicers.
C.	
Edit	the	interactions	of	the	slicer	that	is	on	the	same	page	as	the	KPI	visualization.
D.	
Configure	a	page-level	filter.
E.	
Configure	a	report-level	filter.
Answer:	
BC
Explanation:
Slicers	are	another	way	of	filtering.	They	narrow	the	portion	of	the	dataset	that	is	shown	in	the	other	report
visualizations.
Control	which	page	visuals	are	affected	by	slicers

---

## Question 186
**Énoncé de la question :**
You	have	a	table	that	contains	sales	data	and	approximately	1,000	rows.
You	need	to	identify	outliers	in	the	table.
Which	type	of	visualization	should	you	use?
A.	
area	chart
B.	
scatter	plot
C.	
pie	chart
D.	
donut	chart
Answer:	
B
Explanation:
Outlier	Detection	in	Power	BI	using	Funnel	Plot,	which	is	a	scatter	plot.
Outliers	are	those	data	points	that	lie	outside	the	overall	pattern	of	distribution	&	the	easiest	way	to	detect
outliers	is	though	graphs.	Box	plots,	Scatter	plots	can	help	detect	them	easily.
Reference:
https://towardsdatascience.com/this-article-is-about-identifying-outliers-through-funnel-plots-using-the-mic
rosoft-power-bi-d7ad16ac9ccc
You	have	a	report	that	contains	three	pages.	One	of	the	pages	contains	a	KPI	visualization.
You	need	to	filter	all	the	visualizations	in	the	report	except	for	the	KPI	visualization.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Edit	the	interactions	of	the	KPI	visualization.
B.	
Add	the	same	slicer	to	each	page	and	configure	Sync	slicers.
C.	
Edit	the	interactions	of	the	slicer	that	is	on	the	same	page	as	the	KPI	visualization.
D.	
Configure	a	page-level	filter.
E.	
Configure	a	report-level	filter.
Answer:	
BC
Explanation:
Slicers	are	another	way	of	filtering.	They	narrow	the	portion	of	the	dataset	that	is	shown	in	the	other	report
visualizations.
Control	which	page	visuals	are	affected	by	slicers

**Réponse exacte :**


**Explication courte :**
Box	1:	a	line	-
Incorrect:
*	not	line	and	clustered	column
The	Line	and	Clustered	Column	Chart	is	a	combo	charts	that	combines	the	Line	chart	and	Column	chart
together	in	one	visual.	By	combining	these	two	visuals	together,	you	can	make	a	very	quick	comparison
between	two	sets	of	measures.
Box	2:	anomaly	detection	-
Anomaly	detection	helps	you	enhance	your	line	charts	by	automatically	detecting	anomalies	in	your	time
series	data.	It	also	provides	explanations	for	the	anomalies	to	help	with	root	cause	analysis.	With	just	a	couple
of	clicks,	you	can	easily	find	insights	without	slicing	and	dicing	the	data.
Example:
Reference:
https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-anomaly-detection
You	are	creating	a	Power	BI	report	to	analyze	consumer	purchasing	patterns	from	a	table	named	Transactions.	The
Transactions	table	contains	a	numeric	field	named	Spend.
You	need	to	include	a	visual	that	identifies	which	fields	have	the	greatest	impact	on	Spend.
Which	type	of	visual	should	you	use?
A.	
Q&A
B.	
smart	narrative
C.	
decomposition	tree
D.	
key	influencers
Answer:	
D
Explanation:
The	key	influencers	visual	helps	you	understand	the	factors	that	drive	a	metric	you're	interested	in.	It	analyzes
your	data,	ranks	the	factors	that	matter,	and	displays	them	as	key	influencers.	For	example,	suppose	you	want
to	figure	out	what	influences	employee	turnover,	which	is	also	known	as	churn.	One	factor	might	be
employment	contract	length,	and	another	factor	might	be	commute	time.
When	to	use	key	influencers	-
The	key	influencers	visual	is	a	great	choice	if	you	want	to:
See	which	factors	affect	the	metric	being	analyzed.

---

## Question 187
**Énoncé de la question :**
You	are	creating	a	Power	BI	report	to	analyze	consumer	purchasing	patterns	from	a	table	named	Transactions.	The
Transactions	table	contains	a	numeric	field	named	Spend.
You	need	to	include	a	visual	that	identifies	which	fields	have	the	greatest	impact	on	Spend.
Which	type	of	visual	should	you	use?
A.	
Q&A
B.	
smart	narrative
C.	
decomposition	tree
D.	
key	influencers
Answer:	
D
Explanation:
The	key	influencers	visual	helps	you	understand	the	factors	that	drive	a	metric	you're	interested	in.	It	analyzes
your	data,	ranks	the	factors	that	matter,	and	displays	them	as	key	influencers.	For	example,	suppose	you	want
to	figure	out	what	influences	employee	turnover,	which	is	also	known	as	churn.	One	factor	might	be
employment	contract	length,	and	another	factor	might	be	commute	time.
When	to	use	key	influencers	-
The	key	influencers	visual	is	a	great	choice	if	you	want	to:
See	which	factors	affect	the	metric	being	analyzed.

**Réponse exacte :**


**Explication courte :**
Box	1:	
an	average	reference	line
With	the	Analytics	pane	in	Power	BI	Desktop,	you	can	add	dynamic	reference	lines	to	visuals,	and	provide
focus	for	important	trends	or	insights.
https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-analytics-pane
Box	2:	
Axis

---

## Question 189
**Énoncé de la question :**
Box	2:	
Axis

**Réponse exacte :**
B

**Explication courte :**
With	dashboard	themes	you	can	apply	a	color	theme	to	your	entire	dashboard,	such	as	corporate	colors,
seasonal	coloring,	or	any	other	color	theme	you	might	want	to	apply.	When	you	apply	a	dashboard	theme,	all
visuals	on	your	dashboard	use	the	colors	from	your	selected	theme.
Incorrect:
Not	A:	With	Power	BI	Desktop	report	themes,	you	can	apply	design	changes	to	your	entire	report,	such	as
using	corporate	colors,	changing	icon	sets,	or	applying	new	default	visual	formatting.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-themes
You	have	a	Power	BI	report.	The	report	contains	a	visual	that	shows	gross	sales	by	date.	The	visual	has	anomaly
detection	enabled.
No	anomalies	are	detected.
You	need	to	increase	the	likelihood	that	anomaly	detection	will	identify	anomalies	in	the	report.
What	should	you	do?
A.	
Increase	the	Expected	range	transparency	setting.
B.	
Add	a	data	field	to	the	Legend	field	well.
C.	
Increase	the	Sensitivity	setting.
D.	
Add	a	data	field	to	the	Secondary	values	field	well.
Answer:	
C

---

## Question 191
**Énoncé de la question :**
You	have	a	Power	BI	report.	The	report	contains	a	visual	that	shows	gross	sales	by	date.	The	visual	has	anomaly
detection	enabled.
No	anomalies	are	detected.
You	need	to	increase	the	likelihood	that	anomaly	detection	will	identify	anomalies	in	the	report.
What	should	you	do?
A.	
Increase	the	Expected	range	transparency	setting.
B.	
Add	a	data	field	to	the	Legend	field	well.
C.	
Increase	the	Sensitivity	setting.
D.	
Add	a	data	field	to	the	Secondary	values	field	well.
Answer:	
C

**Réponse exacte :**
A

**Explication courte :**
as	the	requirements,	show	only	value,	so	A,	remove	map	and	charts.
You	have	a	Power	BI	report.
You	have	a	table	named	Data1	that	contains	10	million	rows.
Data1	is	used	in	the	following	visuals:
✑
	A	card	that	shows	the	number	of	records
✑
	A	bar	chart	that	shows	total	transaction	amount	by	territory
✑
	A	scatter	plot	that	shows	transaction	amount	and	profit	amount	on	the	axes	and	points	colored	by	territory
You	need	to	modify	the	scatter	plot	to	make	it	easier	for	users	to	identify	meaningful	patterns.	The	solution	must
not	affect	the	accuracy	of	the	other	visuals.
What	should	you	do?
A.	
Add	a	count	field	of	the	transaction	amount	to	the	size	bucket	of	the	scatter	plot.
B.	
Add	a	trend	line	to	the	scatter	plot.
C.	
Enable	high-density	sampling	on	the	scatter	plot.
D.	
Apply	a	row	filter	to	the	Data1	query	in	Power	Query	Editor.
Answer:	
C
Explanation:
This	question	requires	"modification"	of	the	scatter	plot	and	what	high-density	sampling	essentially	does	is	to
employ	methods	that	capture	and	represent	the	underlying	data	more	effectively	and	eliminates	overlapping
points.
Remember	that	the	table	named	Data1	contains	10	million	rows.	How	do	you	represent	all	that	data	in	a
scatter	plot	in	a	meaningful	pattern	for	easy	understanding	and	analysis?	by	use	of	high	density	sampling.
"By	definition,	high-density	data	is	sampled	to	create	visualizations	reasonably	quickly	that	are	responsive	to
interactivity.	Too	many	data	points	on	a	visual	can	bog	it	down,	and	can	detract	from	the	visibility	of	trends".
This	link	explains	it	more:	https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-high-density-
scatter-charts#how-high-density-scatter-charts-work
You	have	a	Power	BI	workspace	named	Inventory	that	contains	a	dataset,	a	report,	and	a	dashboard.
You	need	to	add	an	additional	tile	to	the	dashboard.	The	tile	must	show	inventory	by	location.	This	information	is
NOT	visualized	in	the	report.	The	solution	must	minimize	the	impact	on	the	report.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Ask	a	question	by	using	Q&A.

---

## Question 193
**Énoncé de la question :**
scatter-charts#how-high-density-scatter-charts-work
You	have	a	Power	BI	workspace	named	Inventory	that	contains	a	dataset,	a	report,	and	a	dashboard.
You	need	to	add	an	additional	tile	to	the	dashboard.	The	tile	must	show	inventory	by	location.	This	information	is
NOT	visualized	in	the	report.	The	solution	must	minimize	the	impact	on	the	report.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
Ask	a	question	by	using	Q&A.

**Réponse exacte :**
AC

**Explication courte :**
In	the	Power	BI	service	(app.powerbi.com),	a	dashboard	contains	tiles	pinned	from	one	or	more	datasets,	so
you	can	ask	questions	about	any	of	the	data	contained	in	any	of	those	datasets.	T
The	answer	to	your	question	is	displayed	as	an	interactive	visualization	and	updates	as	you	modify	the
question.
Open	a	dashboard	and	place	your	cursor	in	the	question	box.	Even	before	you	start	typing,	Q&A	displays	a
new	screen	with	suggestions	to	help	you	form	your	question.	You	see	phrases	and	complete	questions
containing	the	names	of	the	tables	in	the	underlying	datasets	and	may	even	see	complete	questions	listed	if
the	dataset	owner	has	created	featured	questions,
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-tutorial-q-and-a

---

## Question 194
**Énoncé de la question :**
HOTSPOT	-
You	have	a	dataset	named	Pens	that	contains	the	following	columns:
✑
	Item
✑
	Unit	Price
✑
	Quantity	Ordered
You	need	to	create	a	visualization	that	shows	the	relationship	between	Unit	Price	and	Quantity	Ordered.	The
solution	must	highlight	orders	that	have	a	similar	unit	price	and	ordered	quantity.
Which	type	of	visualization	and	which	feature	should	you	use?	To	answer,	select	the	appropriate	options	in	the
answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:
Explanation:
Box	1:	A	scatter	plot	of	Quantity	Ordered	and	Unit	Price	by	item
A	scatter	chart	shows	the	relationship	between	two	numerical	values.
Note:	Scatter	charts	are	a	great	choice:
To	show	relationships	between	two	numerical	values.
To	plot	two	groups	of	numbers	as	one	series	of	x	and	y	coordinates.
To	use	instead	of	a	line	chart	when	you	want	to	change	the	scale	of	the	horizontal	axis.
To	turn	the	horizontal	axis	into	a	logarithmic	scale.
To	display	worksheet	data	that	includes	pairs	or	grouped	sets	of	values.
To	show	patterns	in	large	sets	of	data,	for	example	by	showing	linear	or	non-linear	trends,	clusters,	and

**Réponse exacte :**
C

**Explication courte :**
C.	Sync	the	slicers	on	Page1	and	Page3.
You	have	a	Power	BI	report	that	contains	five	pages.
Pages	1	to	4	are	visible	and	page	5	is	hidden.
You	need	to	create	a	solution	that	will	enable	users	to	quickly	navigate	from	the	first	page	to	all	the	other	visible
pages.	The	solution	must	minimize	development	and	maintenance	effort	as	pages	are	added	to	the	report.
What	should	you	do	first?
A.	
Add	a	blank	button	to	page	1.
B.	
Add	a	page	navigation	button	to	page	1.
C.	
Create	a	bookmark	for	each	page.
D.	
Add	a	bookmark	navigation	button	to	page	1.
Answer:	
B
Explanation:
B	is	correct.	Add	a	page	navigation	button	to	page	1	because	the	solution	must	minimize	development	and
maintenance	effort	as	pages	are	added	to	the	report.	If	we	add	more	pages	the	report	they	will	be
automatically	added	to	the	page	navigator.	Only	thing	is	you	have	to	change	'show	hidden	pages'	option	to	off.
But	with	the	bookmark	navigator,	lot	of	efforts	required	to	create	individual	bookmark	to	each	page	and	also
the	newly	added	pages	manually.	another	problem	is	it	also	adds	all	other	bookmarks	to	the	navigator	which

---

## Question 196
**Énoncé de la question :**
C.	Sync	the	slicers	on	Page1	and	Page3.
You	have	a	Power	BI	report	that	contains	five	pages.
Pages	1	to	4	are	visible	and	page	5	is	hidden.
You	need	to	create	a	solution	that	will	enable	users	to	quickly	navigate	from	the	first	page	to	all	the	other	visible
pages.	The	solution	must	minimize	development	and	maintenance	effort	as	pages	are	added	to	the	report.
What	should	you	do	first?
A.	
Add	a	blank	button	to	page	1.
B.	
Add	a	page	navigation	button	to	page	1.
C.	
Create	a	bookmark	for	each	page.
D.	
Add	a	bookmark	navigation	button	to	page	1.
Answer:	
B
Explanation:
B	is	correct.	Add	a	page	navigation	button	to	page	1	because	the	solution	must	minimize	development	and
maintenance	effort	as	pages	are	added	to	the	report.	If	we	add	more	pages	the	report	they	will	be
automatically	added	to	the	page	navigator.	Only	thing	is	you	have	to	change	'show	hidden	pages'	option	to	off.
But	with	the	bookmark	navigator,	lot	of	efforts	required	to	create	individual	bookmark	to	each	page	and	also
the	newly	added	pages	manually.	another	problem	is	it	also	adds	all	other	bookmarks	to	the	navigator	which

**Réponse exacte :**
C

**Explication courte :**
You	first	have	to	pin	a	one-value	visual	to	the	dashboard	(Card/KPI/Gauge)	and	then	you	can	set	an	alert	on	it's
value.	You	can't	set	alerts	on	a	report	or	whole	report	pages	pinned	to	the	dashboard.
You	have	the	dashboard	shown	in	the	following	exhibit.
You	need	to	modify	the	dashboard	to	display	as	shown	in	the	following	exhibit.

---

## Question 198
**Énoncé de la question :**
You	first	have	to	pin	a	one-value	visual	to	the	dashboard	(Card/KPI/Gauge)	and	then	you	can	set	an	alert	on	it's
value.	You	can't	set	alerts	on	a	report	or	whole	report	pages	pinned	to	the	dashboard.
You	have	the	dashboard	shown	in	the	following	exhibit.
You	need	to	modify	the	dashboard	to	display	as	shown	in	the	following	exhibit.

**Réponse exacte :**
A

**Explication courte :**
The	visual	colors	can't	be	changed	on	the	dashboard	from	a	report	after	the	visual	has	already	been	pinned.
Applying	a	dashboard	custom	theme	will	do	it.
You	need	to	create	a	Power	BI	theme	that	will	be	used	in	multiple	reports.	The	theme	will	include	corporate
branding	for	font	size,	color,	and	bar	chart	formatting.
What	should	you	do?
A.	
From	Power	BI	Desktop,	customize	the	current	theme.
B.	
From	Power	BI	Desktop,	use	a	built-in	report	theme.
C.	
Create	a	theme	as	a	PBIVIZ	file	and	import	the	theme	into	Power	BI	Desktop.
D.	
Create	a	theme	as	a	JSON	file	and	import	the	theme	into	Power	BI	Desktop.
Answer:	
D
Explanation:
D.	Create	a	theme	as	a	JSON	file	and	import	the	theme	into	Power	BI	Desktop.
To	create	a	Power	BI	theme	that	can	be	used	across	multiple	reports	and	workspaces,	the	best	approach
would	be	to	create	a	theme	as	a	JSON	file	and	then	import	it	into	Power	BI	Desktop.	This	will	allow	you	to
define	the	corporate	branding	for	font	size,	color,	and	bar	chart	formatting	in	a	single	file,	which	can	then	be
easily	imported	into	all	the	reports	that	require	it.
To	create	a	theme	as	a	JSON	file,	you	can	use	the	built-in	Theme	Generator	tool	in	Power	BI	or	create	the	file
manually.	Once	you	have	the	JSON	file,	you	can	import	it	into	Power	BI	Desktop	by	going	to	the	"Switch
Theme"	menu	and	selecting	"Import	Theme."	From	there,	you	can	select	the	JSON	file	and	apply	the	theme	to

---

## Question 199
**Énoncé de la question :**
The	visual	colors	can't	be	changed	on	the	dashboard	from	a	report	after	the	visual	has	already	been	pinned.
Applying	a	dashboard	custom	theme	will	do	it.
You	need	to	create	a	Power	BI	theme	that	will	be	used	in	multiple	reports.	The	theme	will	include	corporate
branding	for	font	size,	color,	and	bar	chart	formatting.
What	should	you	do?
A.	
From	Power	BI	Desktop,	customize	the	current	theme.
B.	
From	Power	BI	Desktop,	use	a	built-in	report	theme.
C.	
Create	a	theme	as	a	PBIVIZ	file	and	import	the	theme	into	Power	BI	Desktop.
D.	
Create	a	theme	as	a	JSON	file	and	import	the	theme	into	Power	BI	Desktop.
Answer:	
D
Explanation:
D.	Create	a	theme	as	a	JSON	file	and	import	the	theme	into	Power	BI	Desktop.
To	create	a	Power	BI	theme	that	can	be	used	across	multiple	reports	and	workspaces,	the	best	approach
would	be	to	create	a	theme	as	a	JSON	file	and	then	import	it	into	Power	BI	Desktop.	This	will	allow	you	to
define	the	corporate	branding	for	font	size,	color,	and	bar	chart	formatting	in	a	single	file,	which	can	then	be
easily	imported	into	all	the	reports	that	require	it.
To	create	a	theme	as	a	JSON	file,	you	can	use	the	built-in	Theme	Generator	tool	in	Power	BI	or	create	the	file
manually.	Once	you	have	the	JSON	file,	you	can	import	it	into	Power	BI	Desktop	by	going	to	the	"Switch
Theme"	menu	and	selecting	"Import	Theme."	From	there,	you	can	select	the	JSON	file	and	apply	the	theme	to

**Réponse exacte :**
C

**Explication courte :**
Personalization	can	be	enabled	for	each	visual	or	the	entire	report.	Here	we	have	a	single	page	report	with	3
visuals	and	all	three	visuals	need	personalization,	the	answer	is	'enable	personalization	for	the	entire	report'
to	minimize	development	efforts
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	clustered	bar	chart	that	contains	a	measure	named	Salary	as	the	value	and	a	field	named	Employee	as
the	axis.	Salary	is	present	in	the	data	as	a	numerical	amount	representing	US	dollars.
You	need	to	create	a	reference	line	to	show	which	employees	are	above	the	median	salary.
Solution:	You	create	a	median	line	by	using	the	Salary	measure.
Does	this	meet	the	goal?
A.	
Yes
B.	
No

---

## Question 201
**Énoncé de la question :**
Personalization	can	be	enabled	for	each	visual	or	the	entire	report.	Here	we	have	a	single	page	report	with	3
visuals	and	all	three	visuals	need	personalization,	the	answer	is	'enable	personalization	for	the	entire	report'
to	minimize	development	efforts
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	a	clustered	bar	chart	that	contains	a	measure	named	Salary	as	the	value	and	a	field	named	Employee	as
the	axis.	Salary	is	present	in	the	data	as	a	numerical	amount	representing	US	dollars.
You	need	to	create	a	reference	line	to	show	which	employees	are	above	the	median	salary.
Solution:	You	create	a	median	line	by	using	the	Salary	measure.
Does	this	meet	the	goal?
A.	
Yes
B.	
No

**Réponse exacte :**
A

**Explication courte :**
Answer	is	Yes
We	can	definitely	create	a	median	line	for	the	measure	of	salary	(Tested)
Also	the	other	solution	in	this	series	is	create	a	percentile	line	at	50%	for	the	salary	measure	because
percentile	value	at	50	%	is	exactly	equal	to	the	median	value.
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	a	table	visual	with	a	measure	named	Revenue.	The	Revenue	measure
returns	values	within	a	range	of	0	to	5.
You	need	to	format	the	visual	so	that	the	Revenue	column	displays	a	specific	background	color	based	on	the	value
range	shown	in	the	following	table.
Which	three	actions	should	you	perform	in	sequence	in	Power	BI	Desktop?	To	answer,	move	the	appropriate
actions	from	the	list	of	actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Answer:
Explanation:
Open	the	Background	color	dialog	for	the	revenue	column.
set	format	style	to	rules.
Add	and	configure	a	new	rule	for	each	value	range.

---

## Question 202
**Énoncé de la question :**
Answer	is	Yes
We	can	definitely	create	a	median	line	for	the	measure	of	salary	(Tested)
Also	the	other	solution	in	this	series	is	create	a	percentile	line	at	50%	for	the	salary	measure	because
percentile	value	at	50	%	is	exactly	equal	to	the	median	value.
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	a	table	visual	with	a	measure	named	Revenue.	The	Revenue	measure
returns	values	within	a	range	of	0	to	5.
You	need	to	format	the	visual	so	that	the	Revenue	column	displays	a	specific	background	color	based	on	the	value
range	shown	in	the	following	table.
Which	three	actions	should	you	perform	in	sequence	in	Power	BI	Desktop?	To	answer,	move	the	appropriate
actions	from	the	list	of	actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Answer:
Explanation:
Open	the	Background	color	dialog	for	the	revenue	column.
set	format	style	to	rules.
Add	and	configure	a	new	rule	for	each	value	range.

**Réponse exacte :**
D

**Explication courte :**
Sync	the	Country	slicer	on	page	1,	page	2,	and	page	3.
DRAG	DROP
-
You	use	Power	BI	Desktop	to	create	a	Power	BI	data	model	and	a	blank	report.
You	need	to	add	the	Word	Cloud	visual	shown	in	the	following	exhibit	to	the	report.

---

## Question 204
**Énoncé de la question :**
Sync	the	Country	slicer	on	page	1,	page	2,	and	page	3.
DRAG	DROP
-
You	use	Power	BI	Desktop	to	create	a	Power	BI	data	model	and	a	blank	report.
You	need	to	add	the	Word	Cloud	visual	shown	in	the	following	exhibit	to	the	report.

**Réponse exacte :**


**Explication courte :**
1.	From	Power	BI	Desktop,	get	the	Word	Cloud	visual	from	Microsoft	AppSource
2.	Populate	the	Category,	Value,	and	Excludes	fields
3.	Format	the	data	colors	and	title
(Colors	in	the	Exhibit	are	different	from	the	default	colours)
https://www.youtube.com/watch?v=brkbbS4GSGw
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	five	bookmarks.
You	need	to	add	an	object	to	the	report	from	which	users	can	navigate	between	three	specific	bookmarks.
How	should	you	complete	the	task?	To	answer,	drag	the	appropriate	actions	to	the	correct	steps.	Each	action	may
be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between	panes	or	scroll	to	view
content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
Second	step:	Group	the	three	bookmarks
Third	step:	Change	the	Bookmark	property	for	the	button.

---

## Question 205
**Énoncé de la question :**
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	five	bookmarks.
You	need	to	add	an	object	to	the	report	from	which	users	can	navigate	between	three	specific	bookmarks.
How	should	you	complete	the	task?	To	answer,	drag	the	appropriate	actions	to	the	correct	steps.	Each	action	may
be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar	between	panes	or	scroll	to	view
content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:
Explanation:
Second	step:	Group	the	three	bookmarks
Third	step:	Change	the	Bookmark	property	for	the	button.

**Réponse exacte :**
A

**Explication courte :**
a	paginated	report	that	contains	a	tablix
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	three	pages.	The	pages	are	used	to	analyze	sales	across	various
countries.
You	add	a	slicer	named	Country	to	each	page	of	the	report.
You	need	to	configure	the	report	to	meet	the	following	requirements:
•When	a	user	selects	a	country	on	the	first	page,	the	report	must	filter	the	other	pages.
•The	second	and	third	pages	must	display	only	the	filtered	results.
Which	task	should	you	perform	for	each	requirement?	To	answer,	drag	the	appropriate	task	to	the	correct
requirement.	Each	task	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

---

## Question 207
**Énoncé de la question :**
a	paginated	report	that	contains	a	tablix
DRAG	DROP
-
You	have	a	Power	BI	report	that	contains	three	pages.	The	pages	are	used	to	analyze	sales	across	various
countries.
You	add	a	slicer	named	Country	to	each	page	of	the	report.
You	need	to	configure	the	report	to	meet	the	following	requirements:
•When	a	user	selects	a	country	on	the	first	page,	the	report	must	filter	the	other	pages.
•The	second	and	third	pages	must	display	only	the	filtered	results.
Which	task	should	you	perform	for	each	requirement?	To	answer,	drag	the	appropriate	task	to	the	correct
requirement.	Each	task	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

**Réponse exacte :**


**Explication courte :**
-	Configure	the	Country	slicer	to	sync	across	all	the	pages
-	Hide	the	Country	slicer	on	the	second	and	third	pages
You	have	a	Power	BI	report	that	contains	a	page.	The	page	contains	the	following:
•A	shape	named	Shape1
•A	card	named	Sales	Summary
•A	clustered	bar	chart	named	Sales	by	Region
You	need	to	ensure	that	Sales	Summary	renders	on	top	of	Shape1.
What	should	you	modify?
A.
Tab	order	in	the	Selection	pane
B.
Layer	order	in	the	Selection	pane
C.
Maintain	layer	order	in	the	General	visual	settings
D.
Vertical	alignment	in	the	Canvas	settings
Answer:	
B
Explanation:
B.	Layer	order	in	the	Selection	paneTo	ensure	that	Sales	Summary	renders	on	top	of	Shape1,	you	need	to
adjust	their	layer	order	in	the	Selection	pane.	Power	BI	renders	visuals	based	on	the	layer	order	in	the
Selection	pane,	with	the	topmost	visual	being	rendered	last	and	therefore	appearing	on	top	of	other	visuals.To
adjust	the	layer	order,	you	can	select	the	visuals	in	the	Selection	pane	and	drag	them	up	or	down	to	change
their	position	in	the	layer	order.	In	this	case,	you	would	want	to	select	Sales	Summary	and	drag	it	above
Shape1	in	the	layer	order	to	ensure	it	is	rendered	on	top.
You	have	a	Power	BI	report	named	Report1	and	a	dashboard	named	Dashboard1.	Report1	contains	a	line	chart
named	Sales	by	month.
You	pin	the	Sales	by	month	visual	to	Dashboard1.
In	Report1,	you	change	the	Sales	by	month	visual	to	a	bar	chart.
You	need	to	ensure	that	the	bar	chart	displays	on	Dashboard1.

---

## Question 209
**Énoncé de la question :**
-	Configure	the	Country	slicer	to	sync	across	all	the	pages
-	Hide	the	Country	slicer	on	the	second	and	third	pages
You	have	a	Power	BI	report	that	contains	a	page.	The	page	contains	the	following:
•A	shape	named	Shape1
•A	card	named	Sales	Summary
•A	clustered	bar	chart	named	Sales	by	Region
You	need	to	ensure	that	Sales	Summary	renders	on	top	of	Shape1.
What	should	you	modify?
A.
Tab	order	in	the	Selection	pane
B.
Layer	order	in	the	Selection	pane
C.
Maintain	layer	order	in	the	General	visual	settings
D.
Vertical	alignment	in	the	Canvas	settings
Answer:	
B
Explanation:
B.	Layer	order	in	the	Selection	paneTo	ensure	that	Sales	Summary	renders	on	top	of	Shape1,	you	need	to
adjust	their	layer	order	in	the	Selection	pane.	Power	BI	renders	visuals	based	on	the	layer	order	in	the
Selection	pane,	with	the	topmost	visual	being	rendered	last	and	therefore	appearing	on	top	of	other	visuals.To
adjust	the	layer	order,	you	can	select	the	visuals	in	the	Selection	pane	and	drag	them	up	or	down	to	change
their	position	in	the	layer	order.	In	this	case,	you	would	want	to	select	Sales	Summary	and	drag	it	above
Shape1	in	the	layer	order	to	ensure	it	is	rendered	on	top.
You	have	a	Power	BI	report	named	Report1	and	a	dashboard	named	Dashboard1.	Report1	contains	a	line	chart
named	Sales	by	month.
You	pin	the	Sales	by	month	visual	to	Dashboard1.
In	Report1,	you	change	the	Sales	by	month	visual	to	a	bar	chart.
You	need	to	ensure	that	the	bar	chart	displays	on	Dashboard1.

**Réponse exacte :**
B

**Explication courte :**
B.	Pin	the	Sales	by	month	bar	chart	to	Dashboard1.When	you	pin	a	visual	to	a	dashboard,	you	are	essentially
taking	a	snapshot	of	that	visual	at	that	point	in	time	and	adding	it	to	the	dashboard	as	a	tile.	Any	changes
made	to	the	original	visual	in	the	report	will	not	automatically	reflect	in	the	dashboard	tile.	To	display	the	bar
chart	on	Dashboard1,	you	need	to	pin	the	new	Sales	by	month	bar	chart	to	Dashboard1.
https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-report-change-visualization-type
In	Power	BI	Desktop,	you	are	creating	a	report	that	will	contain	three	pages.
You	need	to	create	a	custom	tooltip	page	and	prepare	the	page	for	use.
Which	three	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
For	the	tooltip	page,	set	Allow	use	as	tooltip	to	On.
B.	
For	the	target	page,	set	Allow	use	as	tooltip	to	On.
C.	
Configure	filters	on	the	target	visual.
D.	
For	the	tooltip	page,	configure	filters.
E.	
Add	and	configure	visuals	on	the	tooltip	page.
Answer:	
ADE
Explanation:
A.	For	the	tooltip	page,	set	Allow	use	as	tooltip	to	On.
D.	For	the	tooltip	page,	configure	filters.
E.	Add	and	configure	visuals	on	the	tooltip	page.
DRAG	DROP
-
You	need	to	use	AI	insights	to	add	a	column	of	enhanced	data	based	on	the	customer	feedback.	The	solution	must
identify	the	following:
•	What	the	customers	most	often	provide	feedback	about

---

## Question 211
**Énoncé de la question :**
In	Power	BI	Desktop,	you	are	creating	a	report	that	will	contain	three	pages.
You	need	to	create	a	custom	tooltip	page	and	prepare	the	page	for	use.
Which	three	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
For	the	tooltip	page,	set	Allow	use	as	tooltip	to	On.
B.	
For	the	target	page,	set	Allow	use	as	tooltip	to	On.
C.	
Configure	filters	on	the	target	visual.
D.	
For	the	tooltip	page,	configure	filters.
E.	
Add	and	configure	visuals	on	the	tooltip	page.
Answer:	
ADE
Explanation:
A.	For	the	tooltip	page,	set	Allow	use	as	tooltip	to	On.
D.	For	the	tooltip	page,	configure	filters.
E.	Add	and	configure	visuals	on	the	tooltip	page.
DRAG	DROP
-
You	need	to	use	AI	insights	to	add	a	column	of	enhanced	data	based	on	the	customer	feedback.	The	solution	must
identify	the	following:
•	What	the	customers	most	often	provide	feedback	about

**Réponse exacte :**


**Explication courte :**
Key	Phrase	Extraction
Sentiment	Analysis
Language	Detection
You	have	a	Power	BI	report	named	ReportA.
You	have	a	Power	BI	tenant	that	allows	users	to	export	data.
You	need	to	ensure	that	consumers	of	ReportA	cannot	export	any	data	from	visuals.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
From	Power	BI	Desktop,	modify	the	Report	settings.
B.	
From	Power	BI	Desktop,	modify	the	Data	Load	settings.

---

## Question 212
**Énoncé de la question :**
Key	Phrase	Extraction
Sentiment	Analysis
Language	Detection
You	have	a	Power	BI	report	named	ReportA.
You	have	a	Power	BI	tenant	that	allows	users	to	export	data.
You	need	to	ensure	that	consumers	of	ReportA	cannot	export	any	data	from	visuals.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.	
From	Power	BI	Desktop,	modify	the	Report	settings.
B.	
From	Power	BI	Desktop,	modify	the	Data	Load	settings.

**Réponse exacte :**
AD

**Explication courte :**
Each	correct	answer	presents	a	complete	solution	so	A	and	D.	You	can	configure	report	settings	both	in
desktop	and	power	bi	service.
You	have	a	Power	BI	report	that	will	be	rendered	on	a	vertical	display.
You	need	to	maximize	the	portion	of	the	screen	area	used	by	the	report.
What	should	you	do?
A.	
From	the	Canvas	background	setting	of	Power	BI	Desktop,	configure	the	Image	fit	setting.
B.	
From	the	Canvas	settings	of	Power	BI	Desktop,	set	a	custom	width	and	height.
C.	
From	Power	BI	Desktop,	select	Personalize	visuals.
D.	
From	the	Power	BI	service,	enable	the	Pages	pane.
Answer:	
B
Explanation:
From	the	Canvas	settings	of	Power	BI	Desktop,	set	a	custom	width	and	height.
You	need	to	create	a	visual	that	compares	profit	across	10	product	categories	fora	selected	quarter.
What	is	the	best	visual	to	use	to	achieve	the	goal?
A.	
an	area	chart
B.	
a	funnel	chart
C.	
a	clustered	bar	chart
D.	
a	line	chart
Answer:	
C
Explanation:
C.	A	clustered	bar	chart.
A	clustered	bar	chart	is	the	best	visual	to	use	to	compare	profit	across	10	product	categories	for	a	selected
quarter.	It	allows	you	to	easily	compare	the	profit	of	each	category	side-by-side,	making	it	easy	to	identify	the
highest	and	lowest	performers.	In	addition,	a	clustered	bar	chart	is	effective	at	displaying	discrete	data,	such
as	categories,	which	makes	it	the	ideal	choice	for	this	scenario.

---

## Question 214
**Énoncé de la question :**
Each	correct	answer	presents	a	complete	solution	so	A	and	D.	You	can	configure	report	settings	both	in
desktop	and	power	bi	service.
You	have	a	Power	BI	report	that	will	be	rendered	on	a	vertical	display.
You	need	to	maximize	the	portion	of	the	screen	area	used	by	the	report.
What	should	you	do?
A.	
From	the	Canvas	background	setting	of	Power	BI	Desktop,	configure	the	Image	fit	setting.
B.	
From	the	Canvas	settings	of	Power	BI	Desktop,	set	a	custom	width	and	height.
C.	
From	Power	BI	Desktop,	select	Personalize	visuals.
D.	
From	the	Power	BI	service,	enable	the	Pages	pane.
Answer:	
B
Explanation:
From	the	Canvas	settings	of	Power	BI	Desktop,	set	a	custom	width	and	height.
You	need	to	create	a	visual	that	compares	profit	across	10	product	categories	fora	selected	quarter.
What	is	the	best	visual	to	use	to	achieve	the	goal?
A.	
an	area	chart
B.	
a	funnel	chart
C.	
a	clustered	bar	chart
D.	
a	line	chart
Answer:	
C
Explanation:
C.	A	clustered	bar	chart.
A	clustered	bar	chart	is	the	best	visual	to	use	to	compare	profit	across	10	product	categories	for	a	selected
quarter.	It	allows	you	to	easily	compare	the	profit	of	each	category	side-by-side,	making	it	easy	to	identify	the
highest	and	lowest	performers.	In	addition,	a	clustered	bar	chart	is	effective	at	displaying	discrete	data,	such
as	categories,	which	makes	it	the	ideal	choice	for	this	scenario.

**Réponse exacte :**
A

**Explication courte :**
you	have	to	have	at	least	build	permissions	on	the	dataset
https://learn.microsoft.com/en-us/power-bi/collaborate-share/service-connect-power-bi-datasets-excel
You	have	a	Power	BI	report	that	contains	a	visual.	The	visual	contains	a	measure.
You	need	to	ensure	that	the	report	meets	the	following	requirements:
•All	values	must	be	set	to	two	decimal	places.
•All	negative	values	must	be	displayed	in	red	font	and	parentheses.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
	For	the	visual,	apply	conditional	formatting	to	the	background	color.
B.
	Configure	the	measure	to	use	a	custom	format.
C.
	For	the	visual,	apply	conditional	formatting	to	the	font	color.
D.
	For	the	visual,	set	Value	decimal	places	to	2.
Answer:	
BC
Explanation:
B	to	format	measure	with	parenthesis	and	decimals	and	c	for	configuring	font	color
Because..	question	each	answer	should	be	part	of	solutions...D.	For	the	visual,	set	Value	decimal	places	to	2,	is
partially	correct	but	it	only	addresses	the	first	requirement	of	setting	all	values	to	two	decimal	places.To
address	the	second	requirement	of	displaying	negative	values	in	red	font	and	parentheses,	we	need	to	apply
conditional	formatting	to	the	font	color	as	stated	in	option	C.Therefore,	we	need	to	perform	both	actions:
configuring	the	measure	to	use	a	custom	format	and	applying	conditional	formatting	to	the	font	color.No
confusion,	and	no	need	to	discuss	further

---

## Question 218
**Énoncé de la question :**
You	have	a	Power	BI	report	that	contains	a	visual.	The	visual	contains	a	measure.
You	need	to	ensure	that	the	report	meets	the	following	requirements:
•All	values	must	be	set	to	two	decimal	places.
•All	negative	values	must	be	displayed	in	red	font	and	parentheses.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	part	of	the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
	For	the	visual,	apply	conditional	formatting	to	the	background	color.
B.
	Configure	the	measure	to	use	a	custom	format.
C.
	For	the	visual,	apply	conditional	formatting	to	the	font	color.
D.
	For	the	visual,	set	Value	decimal	places	to	2.
Answer:	
BC
Explanation:
B	to	format	measure	with	parenthesis	and	decimals	and	c	for	configuring	font	color
Because..	question	each	answer	should	be	part	of	solutions...D.	For	the	visual,	set	Value	decimal	places	to	2,	is
partially	correct	but	it	only	addresses	the	first	requirement	of	setting	all	values	to	two	decimal	places.To
address	the	second	requirement	of	displaying	negative	values	in	red	font	and	parentheses,	we	need	to	apply
conditional	formatting	to	the	font	color	as	stated	in	option	C.Therefore,	we	need	to	perform	both	actions:
configuring	the	measure	to	use	a	custom	format	and	applying	conditional	formatting	to	the	font	color.No
confusion,	and	no	need	to	discuss	further

**Réponse exacte :**


**Explication courte :**
Matrix
Apply	drill	down	filters	to	Selected	Visual
https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions?tabs=powerbi-
desktop#change-the-interactions-of-drillable-visualizationsBy	default,	a	matrix	will	have	"Entire	Page"	in	the
"Apply	drill	down	filters	to"	option	inside	the	Format	tab,	which	is	what	we	don't	want	to	happen,	so	changing
to	"Selected	Visual"	should	give	us	the	behavior	we	want
You	have	a	Power	BI	model	that	contains	two	tables	named	Population	and	Date.
The	Population	table	contains	two	columns	named	PopulationAmount	and	DateKey.
DateKey	contains	date	values	that	represent	the	first	day	of	a	year	and	are	used	to	create	a	many-to-one
relationship	with	the	Date	table.
The	Power	BI	model	contains	two	measures	that	have	the	following	definitions.
Total	Population	=	Sum(‘Population’[PopulationAmount])
2023	Population	=	CALCULATE([Total	Population],	‘Date'[Year]	=	2023)
You	create	a	table	visual	that	displays	Date[Year]	and	[2023	Population].
What	will	the	table	visual	show?
A.
one	row	per	year	that	contains	blank	values	for	every	year	except	2023
B.
one	row	per	date	that	contains	the	population	value	for	the	corresponding	year	repeated	in	each	row
C.
a	single	row	for	the	year	2023	that	contains	the	related	population	value
D.
one	row	per	year	that	contains	the	same	value	repeated	for	each	year
Answer:	
D

---

## Question 219
**Énoncé de la question :**
desktop#change-the-interactions-of-drillable-visualizationsBy	default,	a	matrix	will	have	"Entire	Page"	in	the
"Apply	drill	down	filters	to"	option	inside	the	Format	tab,	which	is	what	we	don't	want	to	happen,	so	changing
to	"Selected	Visual"	should	give	us	the	behavior	we	want
You	have	a	Power	BI	model	that	contains	two	tables	named	Population	and	Date.
The	Population	table	contains	two	columns	named	PopulationAmount	and	DateKey.
DateKey	contains	date	values	that	represent	the	first	day	of	a	year	and	are	used	to	create	a	many-to-one
relationship	with	the	Date	table.
The	Power	BI	model	contains	two	measures	that	have	the	following	definitions.
Total	Population	=	Sum(‘Population’[PopulationAmount])
2023	Population	=	CALCULATE([Total	Population],	‘Date'[Year]	=	2023)
You	create	a	table	visual	that	displays	Date[Year]	and	[2023	Population].
What	will	the	table	visual	show?
A.
one	row	per	year	that	contains	blank	values	for	every	year	except	2023
B.
one	row	per	date	that	contains	the	population	value	for	the	corresponding	year	repeated	in	each	row
C.
a	single	row	for	the	year	2023	that	contains	the	related	population	value
D.
one	row	per	year	that	contains	the	same	value	repeated	for	each	year
Answer:	
D

**Réponse exacte :**


**Explication courte :**
Correct	answer	is:	D.	one	row	per	year	that	contains	the	same	value	repeated	for	each	year.
You	have	a	Power	BI	dataset	that	contains	quarterly	sales	performance	data.
You	need	to	enable	managers	to	review	the	data	in	a	format	that	meets	the	following	requirements:
•Is	optimized	for	printing.
•Renders	data	in	Microsoft	Excel,	Word,	PowerPoint,	and	PDF	formats.
What	should	you	create?
A.
a	template	app
B.
a	dashboard
C.
a	paginated	report
D.
an	interactive	report
Answer:	
C
Explanation:
Correct	answer	is	C:a	paginated	report.
You	have	a	Power	BI	report	that	contains	the	visuals	shown	in	the	following	table.
You	need	to	modify	the	location	of	each	visual.
What	should	you	modify	for	each	visual?
A.
the	layer	order
B.
the	padding
C.
the	position
D.
the	tab	order
Answer:	
C
Explanation:
Correct	answer	is	C:the	position.

---

## Question 221
**Énoncé de la question :**
Correct	answer	is:	D.	one	row	per	year	that	contains	the	same	value	repeated	for	each	year.
You	have	a	Power	BI	dataset	that	contains	quarterly	sales	performance	data.
You	need	to	enable	managers	to	review	the	data	in	a	format	that	meets	the	following	requirements:
•Is	optimized	for	printing.
•Renders	data	in	Microsoft	Excel,	Word,	PowerPoint,	and	PDF	formats.
What	should	you	create?
A.
a	template	app
B.
a	dashboard
C.
a	paginated	report
D.
an	interactive	report
Answer:	
C
Explanation:
Correct	answer	is	C:a	paginated	report.
You	have	a	Power	BI	report	that	contains	the	visuals	shown	in	the	following	table.
You	need	to	modify	the	location	of	each	visual.
What	should	you	modify	for	each	visual?
A.
the	layer	order
B.
the	padding
C.
the	position
D.
the	tab	order
Answer:	
C
Explanation:
Correct	answer	is	C:the	position.

**Réponse exacte :**
AC

**Explication courte :**
A.	a	slicer	visual.
C.	a	table	visual
DRAG	DROP
-
You	plan	to	use	Power	BI	to	create	a	quarterly	profit	report	that	meets	the	following	requirements:
•Emphasizes	the	percentage	of	total	profits	contributed	by	each	product	category	in	dollars	and	as	a	percentage
•Compares	profit	margins	across	sales	regions
Which	type	of	visual	should	you	use	for	each	requirement?	To	answer,	drag	the	appropriate	visuals	to	the	correct
requirements.	Each	visual	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

---

## Question 223
**Énoncé de la question :**
A.	a	slicer	visual.
C.	a	table	visual
DRAG	DROP
-
You	plan	to	use	Power	BI	to	create	a	quarterly	profit	report	that	meets	the	following	requirements:
•Emphasizes	the	percentage	of	total	profits	contributed	by	each	product	category	in	dollars	and	as	a	percentage
•Compares	profit	margins	across	sales	regions
Which	type	of	visual	should	you	use	for	each	requirement?	To	answer,	drag	the	appropriate	visuals	to	the	correct
requirements.	Each	visual	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split	bar
between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

**Réponse exacte :**


**Explication courte :**
Pie	Chart.
Stacked	Bar	Chart.
You	have	the	CSV	file	shown	in	the	following	table.
You	use	Power	Query	Editor	to	preview	the	data	in	the	file.
You	need	to	transform	the	data	to	meet	the	following	requirements:
•The	first	column	must	contain	the	month.
•The	second	column	must	contain	the	year.
•The	third	column	must	contain	the	order	amount	for	the	month	and	year.
Which	transformation	should	you	use	first?
A.
remove
B.
unpivot
C.
transpose
D.
pivot
Answer:	
B
Explanation:
Correct	answer	is	B:unpivot.
You	are	creating	a	Power	BI	single-page	report.
Some	users	will	navigate	the	report	by	using	a	keyboard,	and	some	users	will	navigate	the	report	by	using	a	screen
reader.
You	need	to	ensure	that	the	users	can	consume	content	on	a	report	page	in	a	logical	order.
What	should	you	configure	on	the	report	page?

---

## Question 225
**Énoncé de la question :**
Pie	Chart.
Stacked	Bar	Chart.
You	have	the	CSV	file	shown	in	the	following	table.
You	use	Power	Query	Editor	to	preview	the	data	in	the	file.
You	need	to	transform	the	data	to	meet	the	following	requirements:
•The	first	column	must	contain	the	month.
•The	second	column	must	contain	the	year.
•The	third	column	must	contain	the	order	amount	for	the	month	and	year.
Which	transformation	should	you	use	first?
A.
remove
B.
unpivot
C.
transpose
D.
pivot
Answer:	
B
Explanation:
Correct	answer	is	B:unpivot.
You	are	creating	a	Power	BI	single-page	report.
Some	users	will	navigate	the	report	by	using	a	keyboard,	and	some	users	will	navigate	the	report	by	using	a	screen
reader.
You	need	to	ensure	that	the	users	can	consume	content	on	a	report	page	in	a	logical	order.
What	should	you	configure	on	the	report	page?

**Réponse exacte :**
D

**Explication courte :**
the	tab	order.
You	are	configuring	a	Power	BI	report	for	accessibility	as	shown	in	the	following	table.
You	need	to	change	the	default	colors	of	all	three	visuals	to	make	the	report	more	accessible	to	users	who	have
color	vision	deficiency.
Which	two	settings	should	you	configure	in	the	Customize	theme	window?	Each	correct	answer	presents	part	of
the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
First-level	elements	colors
B.
Theme	colors
C.
Divergent	colors
D.
Sentiment	colors
Answer:	
BC
Explanation:

---

## Question 227
**Énoncé de la question :**
the	tab	order.
You	are	configuring	a	Power	BI	report	for	accessibility	as	shown	in	the	following	table.
You	need	to	change	the	default	colors	of	all	three	visuals	to	make	the	report	more	accessible	to	users	who	have
color	vision	deficiency.
Which	two	settings	should	you	configure	in	the	Customize	theme	window?	Each	correct	answer	presents	part	of
the	solution.
NOTE:	Each	correct	selection	is	worth	one	point.
A.
First-level	elements	colors
B.
Theme	colors
C.
Divergent	colors
D.
Sentiment	colors
Answer:	
BC
Explanation:

**Réponse exacte :**
You	need	to	use	Power	BI	to	create	a	visual	that	will	allow	users	to	compare	the	sales	performance	of	five	sales
regions	for	the	current	month.
Which	visual	should	you	use?
A.
a	line	chart
B.
a	stacked	bar	chart
C.
a	100%	stacked	bar	chart
D.
a	waterfall	chart
Answer:	
B

**Explication courte :**
Correct	answer	is	B:a	stacked	bar	chart.

---

## Question 230
**Énoncé de la question :**
Correct	answer	is	B:a	stacked	bar	chart.
HOTSPOT
-

**Réponse exacte :**
C

**Explication courte :**
Change	the	icons	to	use	a	different	shape	for	each	color.
You	have	a	Power	BI	report	that	contains	one	visual.
You	need	to	provide	users	with	the	ability	to	change	the	visual	type	without	affecting	the	view	for	other	users.
What	should	you	do?
A.
From	the	Bookmarks	pane,	select	Focus	mode,	and	then	select	Add.
B.
From	Report	settings,	select	Personalize	visuals.
C.
From	Visual	options	in	Report	settings,	select	Use	the	modern	visual	header	with	updated	styling	options.
D.
From	Tabular	Editor,	create	a	new	perspective.
Answer:	
B
Explanation:
From	Report	settings,	select	Personalize	visuals.

---

## Question 233
**Énoncé de la question :**
Change	the	icons	to	use	a	different	shape	for	each	color.
You	have	a	Power	BI	report	that	contains	one	visual.
You	need	to	provide	users	with	the	ability	to	change	the	visual	type	without	affecting	the	view	for	other	users.
What	should	you	do?
A.
From	the	Bookmarks	pane,	select	Focus	mode,	and	then	select	Add.
B.
From	Report	settings,	select	Personalize	visuals.
C.
From	Visual	options	in	Report	settings,	select	Use	the	modern	visual	header	with	updated	styling	options.
D.
From	Tabular	Editor,	create	a	new	perspective.
Answer:	
B
Explanation:
From	Report	settings,	select	Personalize	visuals.
HOTSPOT
-
You	have	a	Power	BI	report	that	contains	the	table	visual	shown	in	the	following	exhibit.
You	need	to	modify	the	visual	to	display	as	shown	in	the	following	exhibit.
How	should	you	configure	the	visual?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**
D

**Explication courte :**
Populate	the	alt	text	by	using	conditional	formatting	with	a	DAX	measure.
You	have	a	Power	BI	report	that	contains	a	table	visual.	The	visual	contains	a	column.
The	column	contains	whole	numbers	ranging	from	of	1	to	20.
You	need	to	use	conditional	formatting	to	meet	the	following	requirements:
•Visually	compare	the	values	without	having	to	read	the	text	containing	the	number.
•Show	a	different	format	for	each	distinct	value.
•Hide	the	numeric	value	of	ColumnA.
•Minimize	development	effort.
Which	formatting	should	you	use?
A.
font	color
B.
icons
C.
data	bars
D.
background	color
Answer:	
C
Explanation:
Correct	answer	is	C:data	bars.

---

## Question 235
**Énoncé de la question :**
Populate	the	alt	text	by	using	conditional	formatting	with	a	DAX	measure.
You	have	a	Power	BI	report	that	contains	a	table	visual.	The	visual	contains	a	column.
The	column	contains	whole	numbers	ranging	from	of	1	to	20.
You	need	to	use	conditional	formatting	to	meet	the	following	requirements:
•Visually	compare	the	values	without	having	to	read	the	text	containing	the	number.
•Show	a	different	format	for	each	distinct	value.
•Hide	the	numeric	value	of	ColumnA.
•Minimize	development	effort.
Which	formatting	should	you	use?
A.
font	color
B.
icons
C.
data	bars
D.
background	color
Answer:	
C
Explanation:
Correct	answer	is	C:data	bars.
HOTSPOT
-
You	use	Power	Query	Editor	to	preview	the	data	in	a	column	named	Resource	Location.
The	column	statistics	and	value	distributions	of	Resource	Location	appear	as	shown	in	the	following	exhibit.

**Réponse exacte :**


**Explication courte :**
0
US	East
You	have	a	Power	BI	report	that	contains	the	visual	shown	in	the	following	exhibit.
You	need	to	make	the	visual	more	accessible	to	users	who	have	color	vision	deficiency.
What	should	you	do?
A.
Change	the	font	color	of	values	in	the	Sales	column	to	white.
B.
Change	the	red	background	color	to	orange.
C.
Add	additional	measures	to	the	table	values.
D.
Add	icons	to	represent	the	sales	status	of	each	product.
Answer:	
D
Explanation:
Add	icons	to	represent	the	sales	status	of	each	product.
You	have	a	Power	BI	app	that	contains	a	report	named	Report1.
You	add	a	new	page	to	Report1.
You	need	to	ensure	that	users	can	view	the	new	page.	The	solution	must	minimize	administrative	effort.
What	should	you	do?
A.
Update	the	audience	in	the	app.
B.
Update	the	app.
C.
Update	the	contact	information	in	the	app.

---

## Question 237
**Énoncé de la question :**
0
US	East
You	have	a	Power	BI	report	that	contains	the	visual	shown	in	the	following	exhibit.
You	need	to	make	the	visual	more	accessible	to	users	who	have	color	vision	deficiency.
What	should	you	do?
A.
Change	the	font	color	of	values	in	the	Sales	column	to	white.
B.
Change	the	red	background	color	to	orange.
C.
Add	additional	measures	to	the	table	values.
D.
Add	icons	to	represent	the	sales	status	of	each	product.
Answer:	
D
Explanation:
Add	icons	to	represent	the	sales	status	of	each	product.
You	have	a	Power	BI	app	that	contains	a	report	named	Report1.
You	add	a	new	page	to	Report1.
You	need	to	ensure	that	users	can	view	the	new	page.	The	solution	must	minimize	administrative	effort.
What	should	you	do?
A.
Update	the	audience	in	the	app.
B.
Update	the	app.
C.
Update	the	contact	information	in	the	app.

**Réponse exacte :**
B

**Explication courte :**
Update	the	app.

---

## Question 238
**Énoncé de la question :**
Update	the	app.
HOTSPOT	-
You	have	a	Power	BI	tenant	that	hosts	the	datasets	shown	in	the	following	table.
You	have	the	following	requirements:
The	export	of	reports	that	contain	Personally	Identifiable	Information	(PII)	must	be	prevented.
Data	used	for	financial	decisions	must	be	reviewed	and	approved	before	use.
For	each	of	the	following	statements,	select	Yes	if	the	statement	is	true.	Otherwise,	select	No.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:
Explanation:

**Réponse exacte :**
C

**Explication courte :**
When	you	create	a	sensitivity	label,	you	can	restrict	access	to	content	that	the	label	will	be	applied	to.
When	a	document	or	email	is	encrypted,	access	to	the	content	is	restricted,	so	that	it:
Can	be	decrypted	only	by	users	authorized	by	the	label's	encryption	settings.
Remains	encrypted	no	matter	where	it	resides,	inside	or	outside	your	organization,	even	if	the	file's	renamed.
Incorrect:
Not	B:	Row-level	security	(RLS)	with	Power	BI	can	be	used	to	restrict	data	access	for	given	users.	Filters
restrict	data	access	at	the	row	level,	and	you	can	define	filters	within	roles.
Current	limitations	for	row-level	security:
Reference:
https://docs.microsoft.com/en-us/microsoft-365/compliance/encryption-sensitivity-labels
You	have	a	Microsoft	Excel	file	on	a	file	server.
You	create	a	Power	BI	report	and	import	a	table	from	the	Excel	file.
You	publish	the	report.
You	need	to	ensure	that	the	data	refreshes	every	four	hours.
What	should	you	do	first?
A.	
Upload	the	Excel	file	to	a	Power	BI	workspace.
B.	
Create	a	subscription	to	the	report.
C.	
Deploy	an	on-premises	data	gateway.
D.	
Edit	the	data	source	credentials.
Answer:	
C
Explanation:

---

## Question 240
**Énoncé de la question :**
You	have	a	Microsoft	Excel	file	on	a	file	server.
You	create	a	Power	BI	report	and	import	a	table	from	the	Excel	file.
You	publish	the	report.
You	need	to	ensure	that	the	data	refreshes	every	four	hours.
What	should	you	do	first?
A.	
Upload	the	Excel	file	to	a	Power	BI	workspace.
B.	
Create	a	subscription	to	the	report.
C.	
Deploy	an	on-premises	data	gateway.
D.	
Edit	the	data	source	credentials.
Answer:	
C
Explanation:

**Réponse exacte :**
CD

**Explication courte :**
After	two	months	of	inactivity,	scheduled	refresh	on	your	dataset	is	paused.	A	dataset	is	considered	inactive
when	no	user	has	visited	any	dashboard	or	report	built	on	the	dataset.	At	that	time,	the	dataset	owner	is	sent
an	email	indicating	the	scheduled	refresh	is	paused.	The	refresh	schedule	for	the	dataset	is	then	displayed	as
disabled.	To	resume	scheduled	refresh,	simply	revisit	any	dashboard	or	report	built	on	the	dataset.
Incorrect:
Not	E:	get-powerbireport	retrieves	a	list	of	Power	BI	reports	that	match	the	specified	search	criteria	and
scope.
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/refresh-scheduled-refresh
You	have	a	Power	BI	workspace	that	contains	a	dataset,	a	report,	and	a	dashboard.	The	following	groups	have
access:
✑
	External	users	can	access	the	dashboard.
✑
	Managers	can	access	the	dashboard	and	a	manager-specific	report.
✑
	Employees	can	access	the	dashboard	and	a	row-level	security	(RLS)	constrained	report.
You	need	all	users,	including	the	external	users,	to	be	able	to	tag	workspace	administrators	if	they	identify	an
issue	with	the	dashboard.	The	solution	must	ensure	that	other	users	see	the	issues	that	were	raised.
What	should	you	use?
A.	
comments
B.	
chat	in	Microsoft	Teams
C.	
alerts
D.	
subscriptions
Answer:	
A

---

## Question 242
**Énoncé de la question :**
You	have	a	Power	BI	workspace	that	contains	a	dataset,	a	report,	and	a	dashboard.	The	following	groups	have
access:
✑
	External	users	can	access	the	dashboard.
✑
	Managers	can	access	the	dashboard	and	a	manager-specific	report.
✑
	Employees	can	access	the	dashboard	and	a	row-level	security	(RLS)	constrained	report.
You	need	all	users,	including	the	external	users,	to	be	able	to	tag	workspace	administrators	if	they	identify	an
issue	with	the	dashboard.	The	solution	must	ensure	that	other	users	see	the	issues	that	were	raised.
What	should	you	use?
A.	
comments
B.	
chat	in	Microsoft	Teams
C.	
alerts
D.	
subscriptions
Answer:	
A

**Réponse exacte :**


**Explication courte :**
Add	a	personal	comment	or	start	a	conversation	about	a	dashboard	or	report	with	your	colleagues.	The
comment	feature	is	just	one	of	the	ways	a	business	user	can	collaborate	with	others.
Note:	Comments	can	be	added	to	an	entire	dashboard,	to	individual	visuals	on	a	dashboard,	to	a	report	page,
to	a	paginated	report,	and	to	individual	visuals	on	a	report	page.	Add	a	general	comment	or	add	a	comment
targeted	at	specific	colleagues.
Reference:
https://docs.microsoft.com/en-us/power-bi/consumer/end-user-comment
You	have	a	PBIX	file	that	imports	several	tables	from	an	Azure	SQL	database.
The	data	will	be	migrated	to	another	Azure	SQL	database.
You	need	to	change	the	connections	in	the	PBIX	file.	The	solution	must	minimize	administrative	effort.
What	should	you	do?
A.	
From	Power	Query	Editor,	create	new	queries.
B.	
From	Power	Query	Editor,	modify	the	source	of	each	query.
C.	
Create	a	PBIT	file,	open	the	file,	and	change	the	data	sources	when	prompted.
D.	
Modify	the	Data	source	settings.
Answer:	
D
Explanation:
Open	the	PBIX	file	with	Microsoft	Power	BI	Desktop.
Then	choose	File	->	Options	and	settings	->	Data	source	settings	>Right	click	data	sources	and	change	source.
Note:
Incorrect:
Not	C:	PBIT	is	a	template	file.
The	PBIT	file	keeps	your	report	structure	and	contains	'DataModelSchema	File'	instead	of	''DataModel	File''.
However,	If	you	choose	import	mode,	the	PBIX	file	stores	all	imported	data	from	data	sources	and	the	report
structure.
Reference:
https://windowsreport.com/open-pbix-file/
You	have	a	Power	BI	workspace	that	contains	several	reports.
You	need	to	provide	a	user	with	the	ability	to	create	a	dashboard	that	will	use	the	visuals	from	the	reports.
What	should	you	do?
A.	
Create	a	row-level	security	(RLS)	role	and	add	the	user	to	the	role.
B.	
Share	the	reports	with	the	user.
C.	
Grant	the	Read	permission	for	the	datasets	to	the	user.
D.	
Add	the	user	as	a	member	of	the	workspace.

---

## Question 244
**Énoncé de la question :**
You	have	a	PBIX	file	that	imports	several	tables	from	an	Azure	SQL	database.
The	data	will	be	migrated	to	another	Azure	SQL	database.
You	need	to	change	the	connections	in	the	PBIX	file.	The	solution	must	minimize	administrative	effort.
What	should	you	do?
A.	
From	Power	Query	Editor,	create	new	queries.
B.	
From	Power	Query	Editor,	modify	the	source	of	each	query.
C.	
Create	a	PBIT	file,	open	the	file,	and	change	the	data	sources	when	prompted.
D.	
Modify	the	Data	source	settings.
Answer:	
D
Explanation:
Open	the	PBIX	file	with	Microsoft	Power	BI	Desktop.
Then	choose	File	->	Options	and	settings	->	Data	source	settings	>Right	click	data	sources	and	change	source.
Note:
Incorrect:
Not	C:	PBIT	is	a	template	file.
The	PBIT	file	keeps	your	report	structure	and	contains	'DataModelSchema	File'	instead	of	''DataModel	File''.
However,	If	you	choose	import	mode,	the	PBIX	file	stores	all	imported	data	from	data	sources	and	the	report
structure.
Reference:
https://windowsreport.com/open-pbix-file/
You	have	a	Power	BI	workspace	that	contains	several	reports.
You	need	to	provide	a	user	with	the	ability	to	create	a	dashboard	that	will	use	the	visuals	from	the	reports.
What	should	you	do?
A.	
Create	a	row-level	security	(RLS)	role	and	add	the	user	to	the	role.
B.	
Share	the	reports	with	the	user.
C.	
Grant	the	Read	permission	for	the	datasets	to	the	user.
D.	
Add	the	user	as	a	member	of	the	workspace.

**Réponse exacte :**
D

**Explication courte :**
To	grant	access	to	a	new	workspace,	assign	those	user	groups	or	individuals	to	one	of	the	workspace	roles:
Admin,	Member,	Contributor,	or	Viewer.
Workspace	roles	-
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-roles-new-workspaces
DRAG	DROP	-
You	have	a	Power	BI	workspace	that	contains	a	single-page	report	named	Sales.
You	need	to	add	all	the	visuals	from	Sales	to	a	dashboard.	The	solution	must	ensure	that	additional	visuals	added
to	the	page	are	added	automatically	to	the	dashboard.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:

---

## Question 245
**Énoncé de la question :**
DRAG	DROP	-
You	have	a	Power	BI	workspace	that	contains	a	single-page	report	named	Sales.
You	need	to	add	all	the	visuals	from	Sales	to	a	dashboard.	The	solution	must	ensure	that	additional	visuals	added
to	the	page	are	added	automatically	to	the	dashboard.
Which	three	actions	should	you	perform	in	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Select	and	Place:

**Réponse exacte :**


**Explication courte :**
An	entire	report	page	can	be	pinned	to	a	dashboard,	which	is	called	pinning	a	live	tile.	It's	called	a	live	tile
because	you	can	interact	with	the	tile	on	the	dashboard.
Unlike	with	individual	visualization	tiles,	changes	made	in	the	report	are	automatically	synced	with	the
dashboard.
Step	2:	Open	the	Sales	report	-
Step	3:	Pin	the	page.
1.	Open	a	report	in	Editing	view.
2.	With	no	visualizations	selected,	from	the	menu	bar,	select	Pin	to	a	dashboard.
3.	Pin	the	tile	to	an	existing	dashboard	or	to	a	new	dashboard.	Notice	the	highlighted	text:	Pin	live	page
enables	changes	to	reports	to	appear	in	the	dashboard	tile	when	the	page	is	refreshed.
4.	Select	Pin	live.	A	Success	message	(near	the	top	right	corner)	lets	you	know	the	page	was	added,	as	a	tile,
to	your	dashboard.
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-pin-live-tile-from-report
You	have	a	report	in	Power	BI	named	report1	that	is	based	on	a	shared	dataset.
You	need	to	minimize	the	risk	of	data	exfiltration	for	report.	The	solution	must	prevent	other	reports	from	being
affected.
What	should	you	do?
A.	
Clear	Allow	recipients	to	share	your	dashboard	and	Allow	users	to	build	new	content	using	the	underlying
datasets	for	the	dataset.
B.	
Apply	row-level	security	(RLS)	to	the	shared	dataset.
C.	
Select	the	Allow	end	users	to	export	both	summarized	and	underlying	data	from	the	service	or	Report	Server
Export	data	option	for	the	report.
D.	
Select	the	Don't	allow	end	users	to	export	any	data	from	the	service	or	Report	Server	Export	data	option	for
the	report.
Answer:	
D
Explanation:
Besides	the	various	permissions	you	can	set,	there	are	also	two	different	options	to	disable	the	export
functionality.	First	of	all	is	the	Export	data	in	general	and	second	the	Export	to	Excel	as	a	specific	setting.
Both	have	the	same	setup	for	permissions
Export	Data	-

---

## Question 246
**Énoncé de la question :**
You	have	a	report	in	Power	BI	named	report1	that	is	based	on	a	shared	dataset.
You	need	to	minimize	the	risk	of	data	exfiltration	for	report.	The	solution	must	prevent	other	reports	from	being
affected.
What	should	you	do?
A.	
Clear	Allow	recipients	to	share	your	dashboard	and	Allow	users	to	build	new	content	using	the	underlying
datasets	for	the	dataset.
B.	
Apply	row-level	security	(RLS)	to	the	shared	dataset.
C.	
Select	the	Allow	end	users	to	export	both	summarized	and	underlying	data	from	the	service	or	Report	Server
Export	data	option	for	the	report.
D.	
Select	the	Don't	allow	end	users	to	export	any	data	from	the	service	or	Report	Server	Export	data	option	for
the	report.
Answer:	
D
Explanation:
Besides	the	various	permissions	you	can	set,	there	are	also	two	different	options	to	disable	the	export
functionality.	First	of	all	is	the	Export	data	in	general	and	second	the	Export	to	Excel	as	a	specific	setting.
Both	have	the	same	setup	for	permissions
Export	Data	-

**Réponse exacte :**
D

**Explication courte :**
1.)	in	Power	BI	Desktop	>	File	>	Options	>	Report	Settings	>	Export	data	>	Allow	end	users	to	export	data	with
current	layout,	summarize	data	and	underlying	data	from	the	service	or	Report	Server.
2.)	in	Power	BI	Service	in	Report	Settings	>	Export	data	section	I	found:	"Choose	the	type	of	data	you	allow
your	end	users	to	export."	Here	you	can	select	one	option	from:
-	Summarized	data	and	data	with	current	layout
-	Summarized	data,	with	current	layout	and	underlying	data
-	None

---

## Question 247
**Énoncé de la question :**
1.)	in	Power	BI	Desktop	>	File	>	Options	>	Report	Settings	>	Export	data	>	Allow	end	users	to	export	data	with
current	layout,	summarize	data	and	underlying	data	from	the	service	or	Report	Server.
2.)	in	Power	BI	Service	in	Report	Settings	>	Export	data	section	I	found:	"Choose	the	type	of	data	you	allow
your	end	users	to	export."	Here	you	can	select	one	option	from:
-	Summarized	data	and	data	with	current	layout
-	Summarized	data,	with	current	layout	and	underlying	data
-	None

**Réponse exacte :**
C

**Explication courte :**
Configure	row-level	security	group	membership,	Working	with	members
Add	members	-
In	the	Power	BI	service,	you	can	add	a	member	to	the	role	by	typing	in	the	email	address	or	name	of	the	user
or	security	group.
You	can	use	the	following	groups	to	set	up	row	level	security.
Distribution	Group	-
Mail-enabled	Group	-
Security	Group	-
Incorrect:
Not	A:	Build	permission	applies	to	datasets.	When	you	give	users	Build	permission,	they	can	build	new	content
on	your	dataset,	such	as	reports,	dashboards,	pinned	tiles	from	Q&A,	paginated	reports,	and	Insights
Discovery.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls

---

## Question 248
**Énoncé de la question :**
Configure	row-level	security	group	membership,	Working	with	members
Add	members	-
In	the	Power	BI	service,	you	can	add	a	member	to	the	role	by	typing	in	the	email	address	or	name	of	the	user
or	security	group.
You	can	use	the	following	groups	to	set	up	row	level	security.
Distribution	Group	-
Mail-enabled	Group	-
Security	Group	-
Incorrect:
Not	A:	Build	permission	applies	to	datasets.	When	you	give	users	Build	permission,	they	can	build	new	content
on	your	dataset,	such	as	reports,	dashboards,	pinned	tiles	from	Q&A,	paginated	reports,	and	Insights
Discovery.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls

**Réponse exacte :**
D

**Explication courte :**
You	can	use	the	following	groups	to	set	up	row	level	security.
*	Distribution	Group
*	Mail-enabled	Group	-	This	group	also	contains	a	list	of	email	addresses	of	members	and	can	also	be	used	to
control	access	to	OneDrive	and	SharePoint.
The	Mail-Enabled	Security	Group	can	be	created	in	the	Office	365	Admin	Portal.
*	Security	Group	-	This	is	also	known	as	an	Active	Directory	Security	Group.	This	group	lives	within	Active
Directory	and	Azure	Active	Directory.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls	https://www.fourmoo.com/2020/04/0
1/power-bi-which-groups-can-be-used-to-set-permissions-in-power-bi/
You	have	more	than	100	published	datasets.
Ten	of	the	datasets	were	verified	to	meet	your	corporate	quality	standards.
You	need	to	ensure	that	the	10	verified	datasets	appear	at	the	top	of	the	list	of	published	datasets	whenever	users
search	for	existing	datasets.
What	should	you	do?
A.	
Promote	the	datasets.
B.	
Certify	the	datasets.
C.	
Feature	the	dataset	on	the	home	page.
D.	
Publish	the	datasets	in	an	app.
Answer:	
B
Explanation:
Once	logged	in,	you	will	be	presented	with	a	list	of	datasets	that	you	can	access	from	your	various
workspaces.	This	is	one	reason	why	having	official	datasets	promoted	and	certified	is	recommended,	as	these
will	appear	at	the	top	of	the	list,	with	certified	datasets	appearing	before	promoted	datasets.
Note:	Power	BI	provides	two	ways	you	can	endorse	your	valuable,	high-quality	content	to	increase	its	visibility:
promotion	and	certification.
Promotion:	Promotion	is	a	way	to	highlight	content	you	think	is	valuable	and	worthwhile	for	others	to	use.	It
encourages	the	collaborative	use	and	spread	of	content	within	an	organization.
Any	content	owner,	as	well	as	any	member	with	write	permissions	on	the	workspace	where	the	content	is

---

## Question 251
**Énoncé de la question :**
https://www.fourmoo.com/2020/04/0
1/power-bi-which-groups-can-be-used-to-set-permissions-in-power-bi/
You	have	more	than	100	published	datasets.
Ten	of	the	datasets	were	verified	to	meet	your	corporate	quality	standards.
You	need	to	ensure	that	the	10	verified	datasets	appear	at	the	top	of	the	list	of	published	datasets	whenever	users
search	for	existing	datasets.
What	should	you	do?
A.	
Promote	the	datasets.
B.	
Certify	the	datasets.
C.	
Feature	the	dataset	on	the	home	page.
D.	
Publish	the	datasets	in	an	app.
Answer:	
B
Explanation:
Once	logged	in,	you	will	be	presented	with	a	list	of	datasets	that	you	can	access	from	your	various
workspaces.	This	is	one	reason	why	having	official	datasets	promoted	and	certified	is	recommended,	as	these
will	appear	at	the	top	of	the	list,	with	certified	datasets	appearing	before	promoted	datasets.
Note:	Power	BI	provides	two	ways	you	can	endorse	your	valuable,	high-quality	content	to	increase	its	visibility:
promotion	and	certification.
Promotion:	Promotion	is	a	way	to	highlight	content	you	think	is	valuable	and	worthwhile	for	others	to	use.	It
encourages	the	collaborative	use	and	spread	of	content	within	an	organization.
Any	content	owner,	as	well	as	any	member	with	write	permissions	on	the	workspace	where	the	content	is

**Réponse exacte :**


**Explication courte :**
Box	1:	
Member	-
Only	Admin	and	Member	can	publish,	unpublish,	and	change	permissions	for	an	app.
Incorrect:
Contributors	can	update	the	app	associated	with	the	workspace,	if	the	workspace	Admin	delegates	this
permission	to	them.	However,	they	can't	publish	a	new	app	or	change	who	has	permission	to	it.
Box	2:	
Contributor	-
Admin	,	Member	and	Contributor	can	create,	edit,	and	delete	content,	such	as	reports,	in	the	workspace.
Note:	Contributor	-	This	role	can	access	and	interact	with	reports	and	dashboards.	Additionally,	this	role	can
create,	edit,	copy,	and	delete	items	in	a	workspace,	publish	reports,	schedule	refreshes,	and	modify	gateways.
Incorrect:
Viewer	-	This	role	provides	read	only	access	to	workspace	items.	Read	access	does	provide	report	/	dashboard
consumers	the	ability	to	not	only	view,	but	also	interact	with	visuals.	Interaction	does	not	mean	changing	a
visual.
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-roles-new-workspaces
https://www.mssqltips.com/sqlservertip/6487/power-bi-workspace-permissions-and-roles
You	create	a	dashboard	by	using	the	Microsoft	Power	BI	Service.	The	dashboard	contains	a	card	visual	that	shows
total	sales	from	the	current	year.
You	grant	users	access	to	the	dashboard	by	using	the	Viewer	role	on	the	workspace.
A	user	wants	to	receive	daily	notifications	of	the	number	shown	on	the	card	visual.
You	need	to	automate	the	notifications.
What	should	you	do?
A.	
Create	a	subscription.
B.	
Create	a	data	alert.
C.	
Share	the	dashboard	to	the	user.
D.	
Tag	the	user	in	a	comment.
Answer:	
A
Explanation:
A	is	correct,	you	need	a	subscription,	not	an	alert	as	alerts	don't	include	a	snapshot	and	they	will	only	be	sent
based	on	a	certain	condition	whereas	here	you	want	daily	notifications,	not	just	when	the	value	exceeds	a
certain	threshold.
You	have	a	Power	BI	workspace	named	Workspace1	that	contains	a	dataset	named	DS1	and	a	report	named	RPT1.
A	user	wants	to	create	a	report	by	using	the	data	in	DS1	and	publish	the	report	to	another	workspace.
You	need	to	provide	the	user	with	the	appropriate	access.	The	solution	must	minimize	the	number	of	access
permissions	granted	to	the	user.
What	should	you	do?
A.	
Add	the	user	as	a	Viewer	of	Workspace1.
B.	
Grant	the	Build	permission	for	DS1	to	the	user.
C.	
Share	RPT1	with	the	user.
D.	
Add	the	user	as	a	member	of	Workspace1.
Answer:	
B
Explanation:

---

## Question 253
**Énoncé de la question :**
https://www.mssqltips.com/sqlservertip/6487/power-bi-workspace-permissions-and-roles
You	create	a	dashboard	by	using	the	Microsoft	Power	BI	Service.	The	dashboard	contains	a	card	visual	that	shows
total	sales	from	the	current	year.
You	grant	users	access	to	the	dashboard	by	using	the	Viewer	role	on	the	workspace.
A	user	wants	to	receive	daily	notifications	of	the	number	shown	on	the	card	visual.
You	need	to	automate	the	notifications.
What	should	you	do?
A.	
Create	a	subscription.
B.	
Create	a	data	alert.
C.	
Share	the	dashboard	to	the	user.
D.	
Tag	the	user	in	a	comment.
Answer:	
A
Explanation:
A	is	correct,	you	need	a	subscription,	not	an	alert	as	alerts	don't	include	a	snapshot	and	they	will	only	be	sent
based	on	a	certain	condition	whereas	here	you	want	daily	notifications,	not	just	when	the	value	exceeds	a
certain	threshold.
You	have	a	Power	BI	workspace	named	Workspace1	that	contains	a	dataset	named	DS1	and	a	report	named	RPT1.
A	user	wants	to	create	a	report	by	using	the	data	in	DS1	and	publish	the	report	to	another	workspace.
You	need	to	provide	the	user	with	the	appropriate	access.	The	solution	must	minimize	the	number	of	access
permissions	granted	to	the	user.
What	should	you	do?
A.	
Add	the	user	as	a	Viewer	of	Workspace1.
B.	
Grant	the	Build	permission	for	DS1	to	the	user.
C.	
Share	RPT1	with	the	user.
D.	
Add	the	user	as	a	member	of	Workspace1.
Answer:	
B
Explanation:

**Réponse exacte :**
A

**Explication courte :**
The	answer	is	A..Yes
When	you	publish	an	app	in	Power	BI,	you	can	select	the	specific	content	you	want	to	include	in	the	app,	such
as	reports	and	dashboards,	and	specify	the	access	levels	for	each	item.	You	can	also	choose	to	make	the	app
available	to	specific	users	or	groups,	or	publish	it	to	the	entire	organization.
If	you	publish	an	app	to	the	entire	organization,	all	users	in	your	organization	would	have	access	to	the	app
and	its	included	content,	as	long	as	they	have	a	Power	BI	license.	You	can	set	the	appropriate	access	level	for
each	item	in	the	app,	such	as	read-only	access	for	the	selected	dashboard	and	reports,	to	ensure	that	users
only	have	access	to	the	content	they	need.
Therefore,	publishing	an	app	to	the	entire	organization	with	the	appropriate	access	levels	for	the	dashboard
and	reports	would	meet	the	goal	of	granting	all	organizational	users	read	access	to	one	dashboard	and	three
reports.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series

---

## Question 255
**Énoncé de la question :**
The	answer	is	A..Yes
When	you	publish	an	app	in	Power	BI,	you	can	select	the	specific	content	you	want	to	include	in	the	app,	such
as	reports	and	dashboards,	and	specify	the	access	levels	for	each	item.	You	can	also	choose	to	make	the	app
available	to	specific	users	or	groups,	or	publish	it	to	the	entire	organization.
If	you	publish	an	app	to	the	entire	organization,	all	users	in	your	organization	would	have	access	to	the	app
and	its	included	content,	as	long	as	they	have	a	Power	BI	license.	You	can	set	the	appropriate	access	level	for
each	item	in	the	app,	such	as	read-only	access	for	the	selected	dashboard	and	reports,	to	ensure	that	users
only	have	access	to	the	content	they	need.
Therefore,	publishing	an	app	to	the	entire	organization	with	the	appropriate	access	levels	for	the	dashboard
and	reports	would	meet	the	goal	of	granting	all	organizational	users	read	access	to	one	dashboard	and	three
reports.
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series

**Réponse exacte :**
B

**Explication courte :**
You	need	to	specify	the	dashboard	and	the	three	reports	to	be	included	in	the	app.
Instead:	You	create	an	Azure	Active	Directory	group	that	contains	all	the	users.	You	share	each	selected
report	and	the	one	dashboard	to	the	group.
Note:	A	published	App	can	provide	the	required	access.
When	the	dashboards	and	reports	in	your	workspace	are	ready,	you	choose	which	dashboards	and	reports	you
want	to	publish,	then	publish	them	as	an	app.
In	Power	BI,	you	can	create	official	packaged	content,	then	distribute	it	to	a	broad	audience	as	an	app.	You
create	apps	in	workspaces,	where	you	can	collaborate	on	Power	BI	content	with	your	colleagues.	Then	you
can	publish	the	finished	app	to	large	groups	of	people	in	your	organization.
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-distribute-apps
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	five	reports	and	two	dashboards	in	a	workspace.
You	need	to	grant	all	organizational	users	read	access	to	one	dashboard	and	three	reports.
Solution:	You	assign	all	the	users	the	Viewer	role	to	the	workspace.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
In	this	way	all	users	will	see	all	workspace	content	not	only	the	one	dashboard	and	3	reports
From	Power	BI	Desktop,	you	publish	a	new	dataset	and	report	to	a	Power	BI	workspace.	The	dataset	has	a	row-
level	security	(RLS)	role	named	HR.
You	need	to	ensure	that	the	HR	team	members	have	RLS	applied	when	they	view	reports	based	on	the	dataset.
What	should	you	do?

---

## Question 257
**Énoncé de la question :**
Note:	This	question	is	part	of	a	series	of	questions	that	present	the	same	scenario.	Each	question	in	the	series
contains	a	unique	solution	that	might	meet	the	stated	goals.	Some	question	sets	might	have	more	than	one	correct
solution,	while	others	might	not	have	a	correct	solution.
After	you	answer	a	question	in	this	section,	you	will	NOT	be	able	to	return	to	it.	As	a	result,	these	questions	will	not
appear	in	the	review	screen.
You	have	five	reports	and	two	dashboards	in	a	workspace.
You	need	to	grant	all	organizational	users	read	access	to	one	dashboard	and	three	reports.
Solution:	You	assign	all	the	users	the	Viewer	role	to	the	workspace.
Does	this	meet	the	goal?
A.	
Yes
B.	
No
Answer:	
B
Explanation:
In	this	way	all	users	will	see	all	workspace	content	not	only	the	one	dashboard	and	3	reports
From	Power	BI	Desktop,	you	publish	a	new	dataset	and	report	to	a	Power	BI	workspace.	The	dataset	has	a	row-
level	security	(RLS)	role	named	HR.
You	need	to	ensure	that	the	HR	team	members	have	RLS	applied	when	they	view	reports	based	on	the	dataset.
What	should	you	do?

**Réponse exacte :**
A

**Explication courte :**
Working	with	members	-
Add	members	-
In	the	Power	BI	service,	you	can	add	a	member	to	the	role	by	typing	in	the	email	address	or	name	of	the	user
or	security	group.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls
You	have	a	Power	BI	dashboard	that	monitors	the	quality	of	manufacturing	processes.	The	dashboard	contains	the
following	elements:
✑
	A	line	chart	that	shows	the	number	of	defective	products	manufactured	by	day
✑
	A	KPI	visual	that	shows	the	current	daily	percentage	of	defective	products	manufactured
You	need	to	be	notified	when	the	daily	percentage	of	defective	products	manufactured	exceeds	3%.
What	should	you	create?
A.	
a	subscription
B.	
an	alert
C.	
a	smart	narrative	visual
D.	
a	Q&A	visual
Answer:	
B
Explanation:
Set	alerts	in	the	Power	BI	service	to	notify	you	when	data	on	a	dashboard	changes	above	or	below	limits	you
set.	Alerts	can	be	set	on	tiles	pinned	from	report	visuals	or	from	Power	BI	Q&A,	and	only	on	gauges,	KPIs,	and
cards.
Reference:
https://docs.microsoft.com/en-us/power-bi/consumer/end-user-alerts
You	create	a	report	by	using	Microsoft	Power	BI	Desktop.
The	report	uses	data	from	a	Microsoft	SQL	Server	Analysis	Services	(SSAS)	cube	located	on	your	company's
internal	network.
You	plan	to	publish	the	report	to	the	Power	BI	Service.
What	should	you	implement	to	ensure	that	users	who	consume	the	report	from	the	Power	BI	Service	have	the	most
up-to-date	data	from	the	cube?
A.	
an	OData	feed

---

## Question 259
**Énoncé de la question :**
You	have	a	Power	BI	dashboard	that	monitors	the	quality	of	manufacturing	processes.	The	dashboard	contains	the
following	elements:
✑
	A	line	chart	that	shows	the	number	of	defective	products	manufactured	by	day
✑
	A	KPI	visual	that	shows	the	current	daily	percentage	of	defective	products	manufactured
You	need	to	be	notified	when	the	daily	percentage	of	defective	products	manufactured	exceeds	3%.
What	should	you	create?
A.	
a	subscription
B.	
an	alert
C.	
a	smart	narrative	visual
D.	
a	Q&A	visual
Answer:	
B
Explanation:
Set	alerts	in	the	Power	BI	service	to	notify	you	when	data	on	a	dashboard	changes	above	or	below	limits	you
set.	Alerts	can	be	set	on	tiles	pinned	from	report	visuals	or	from	Power	BI	Q&A,	and	only	on	gauges,	KPIs,	and
cards.
Reference:
https://docs.microsoft.com/en-us/power-bi/consumer/end-user-alerts
You	create	a	report	by	using	Microsoft	Power	BI	Desktop.
The	report	uses	data	from	a	Microsoft	SQL	Server	Analysis	Services	(SSAS)	cube	located	on	your	company's
internal	network.
You	plan	to	publish	the	report	to	the	Power	BI	Service.
What	should	you	implement	to	ensure	that	users	who	consume	the	report	from	the	Power	BI	Service	have	the	most
up-to-date	data	from	the	cube?
A.	
an	OData	feed

**Réponse exacte :**
B

**Explication courte :**
After	you	install	the	on-premises	data	gateway,	you	need	to	add	data	sources	that	can	be	used	with	the
gateway.	You	can	work	with	gateways	and	SQL	Server
Analysis	Services	(SSAS)	data	sources	that	are	used	either	for	scheduled	refresh	or	for	live	connections.
Note:	Power	BI	service	is	a	cloud-based	business	analytics	and	data	visualization	service	that	enables	anyone
to	visualize	and	analyze	data	with	greater	speed,	efficiency,	and	understanding.
Reference:
https://docs.microsoft.com/en-us/power-bi/connect-data/service-gateway-enterprise-manage-ssas
You	have	five	sales	regions.	Each	region	is	assigned	a	single	salesperson.
You	have	an	imported	dataset	that	has	a	dynamic	row-level	security	(RLS)	role	named	Sales.	The	Sales	role	filters
sales	transaction	data	by	salesperson.
Salespeople	must	see	only	the	data	from	their	region.
You	publish	the	dataset	to	powerbi.com,	set	RLS	role	membership,	and	distribute	the	dataset	and	related	reports
to	the	salespeople.
A	salesperson	reports	that	she	believes	she	should	see	more	data.
You	need	to	verify	what	data	the	salesperson	currently	sees.
What	should	you	do?
A.	
Use	the	Test	as	role	option	to	view	data	as	the	salesperson's	user	account.
B.	
Use	the	Test	as	role	option	to	view	data	as	the	Sales	role.
C.	
Instruct	the	salesperson	to	open	the	report	in	Microsoft	Power	BI	Desktop.
D.	
Filter	the	data	in	the	reports	to	match	the	intended	logic	in	the	filter	on	the	sales	transaction	table.
Answer:	
A
Explanation:
	A,	to	be	able	to	see	what	the	specific	salesperson	sees	(and	compare	it	to	what	she	should	see)	you	should
test	the	report	as	that	user	account	since	the	RLS	is	dynamic	and	based	on	the	user	accounts.
You	have	multiple	dashboards.
You	need	to	ensure	that	when	users	browse	the	available	dashboards	from	powerbi.com,	they	can	see	which
dashboards	contain	Personally	Identifiable
Information	(PII).	The	solution	must	minimize	configuration	effort	and	impact	on	the	dashboard	design.
What	should	you	use?
A.	
Microsoft	Information	Protection	sensitivity	labels
B.	
tiles
C.	
comments
D.	
Active	Directory	groups

---

## Question 261
**Énoncé de la question :**
You	have	five	sales	regions.	Each	region	is	assigned	a	single	salesperson.
You	have	an	imported	dataset	that	has	a	dynamic	row-level	security	(RLS)	role	named	Sales.	The	Sales	role	filters
sales	transaction	data	by	salesperson.
Salespeople	must	see	only	the	data	from	their	region.
You	publish	the	dataset	to	powerbi.com,	set	RLS	role	membership,	and	distribute	the	dataset	and	related	reports
to	the	salespeople.
A	salesperson	reports	that	she	believes	she	should	see	more	data.
You	need	to	verify	what	data	the	salesperson	currently	sees.
What	should	you	do?
A.	
Use	the	Test	as	role	option	to	view	data	as	the	salesperson's	user	account.
B.	
Use	the	Test	as	role	option	to	view	data	as	the	Sales	role.
C.	
Instruct	the	salesperson	to	open	the	report	in	Microsoft	Power	BI	Desktop.
D.	
Filter	the	data	in	the	reports	to	match	the	intended	logic	in	the	filter	on	the	sales	transaction	table.
Answer:	
A
Explanation:
	A,	to	be	able	to	see	what	the	specific	salesperson	sees	(and	compare	it	to	what	she	should	see)	you	should
test	the	report	as	that	user	account	since	the	RLS	is	dynamic	and	based	on	the	user	accounts.
You	have	multiple	dashboards.
You	need	to	ensure	that	when	users	browse	the	available	dashboards	from	powerbi.com,	they	can	see	which
dashboards	contain	Personally	Identifiable
Information	(PII).	The	solution	must	minimize	configuration	effort	and	impact	on	the	dashboard	design.
What	should	you	use?
A.	
Microsoft	Information	Protection	sensitivity	labels
B.	
tiles
C.	
comments
D.	
Active	Directory	groups

**Réponse exacte :**
A

**Explication courte :**
In	the	Power	BI	service,	sensitivity	labels	can	be	applied	to	datasets,	reports,	dashboards,	and	dataflows.
Sensitivity	labels	on	reports,	dashboards,	datasets,	and	dataflows	are	visible	from	many	places	in	the	Power
BI	service.	Sensitivity	labels	on	reports	and	dashboards	are	also	visible	in	the	Power	BI	iOS	and	Android	mobile
apps	and	in	embedded	visuals.	In	Desktop,	you	can	see	the	sensitivity	label	in	the	status	bar.
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-security-sensitivity-label-overview

---

## Question 262
**Énoncé de la question :**
HOTSPOT	-
You	have	a	dataset	that	has	the	permissions	shown	in	the	following	exhibit.
Use	the	drop-down	menus	to	select	the	answer	choice	that	completes	each	statement	based	on	the	information
presented	in	the	graphic.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:
Explanation:
Box	1:	use	Analyze	in	Excel	-

**Réponse exacte :**
A

**Explication courte :**
Yes,	from	the	documentation	a	suggestion	made	there	to	share	with	more	than	100	separate	users	is	to	"Share
with	a	user	group	that	contains	all	the
DRAG	DROP	-
You	have	a	Power	BI	table	named	Customer	that	contains	a	field	named	Email	Address.
You	discover	that	multiple	records	contain	the	same	email	address.
You	need	to	create	a	calculated	column	to	identify	which	records	have	duplicate	email	addresses.
How	should	you	complete	the	DAX	expression	for	the	calculated	column?	To	answer,	drag	the	appropriate	values
to	the	correct	targets.	Each	value	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split
bar	between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:

---

## Question 264
**Énoncé de la question :**
Yes,	from	the	documentation	a	suggestion	made	there	to	share	with	more	than	100	separate	users	is	to	"Share
with	a	user	group	that	contains	all	the
DRAG	DROP	-
You	have	a	Power	BI	table	named	Customer	that	contains	a	field	named	Email	Address.
You	discover	that	multiple	records	contain	the	same	email	address.
You	need	to	create	a	calculated	column	to	identify	which	records	have	duplicate	email	addresses.
How	should	you	complete	the	DAX	expression	for	the	calculated	column?	To	answer,	drag	the	appropriate	values
to	the	correct	targets.	Each	value	may	be	used	once,	more	than	once,	or	not	at	all.	You	may	need	to	drag	the	split
bar	between	panes	or	scroll	to	view	content.
NOTE:	Each	correct	selection	is	worth	one	point.
Select	and	Place:

**Réponse exacte :**


**Explication courte :**
Calculate
Countrows
All
DRAG	DROP
-
You	publish	a	dataset	that	contains	data	from	an	on-premises	Microsoft	SQL	Server	database.
The	dataset	must	be	refreshed	daily.
You	need	to	ensure	that	the	Power	BI	service	can	connect	to	the	database	and	refresh	the	dataset.
Which	four	actions	should	you	perform	n	sequence?	To	answer,	move	the	appropriate	actions	from	the	list	of
actions	to	the	answer	area	and	arrange	them	in	the	correct	order.
Answer:
Explanation:
https://learn.microsoft.com/en-us/data-integration/gateway/service-gateway-install
https://learn.microsoft.com/en-us/power-bi/connect-data/service-gateway-sql-tutorial
You	have	a	Power	BI	dataset	and	a	connected	report.

---

## Question 266
**Énoncé de la question :**
https://learn.microsoft.com/en-us/power-bi/connect-data/service-gateway-sql-tutorial
You	have	a	Power	BI	dataset	and	a	connected	report.

**Réponse exacte :**
D

**Explication courte :**
The	correct	answer	is	D.	C	is	incorrect	because	if	you	change	the	export	data	setting	to	None,	users	will	not	be
able	to	export	the	data	in	any	form.
By	providing	the	users	with	Summarized	data,	data	with	current	layout	and	underlying	data	option,	it	will	not
change	the	way	data	is	visualized	in	the	report,	but	it	allows	the	users	to	download	the	data	and	analyze	it	with
Excel.

---

## Question 267
**Énoncé de la question :**
The	correct	answer	is	D.	C	is	incorrect	because	if	you	change	the	export	data	setting	to	None,	users	will	not	be
able	to	export	the	data	in	any	form.
By	providing	the	users	with	Summarized	data,	data	with	current	layout	and	underlying	data	option,	it	will	not
change	the	way	data	is	visualized	in	the	report,	but	it	allows	the	users	to	download	the	data	and	analyze	it	with
Excel.
HOTSPOT
-
You	have	two	Power	BI	workspaces	named	WorkspaceA	and	WorkspaceB.	WorkspaceA	contains	two	datasets
named	Sales	and	HR.
You	need	to	provide	a	user	named	User1	with	access	to	the	WorkspaceB.	The	solution	must	meet	the	following
requirements:
•	Create	reports	that	use	the	HR	dataset.
•	Publish	the	reports	to	WorkspaceB.
•	Prevent	the	ability	to	modify	the	HR	dataset.
•	Prevent	the	ability	to	add	users	to	Workspaces.
What	should	you	do?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**


**Explication courte :**
Grant	User	1	the	Build	Permission	for	the	HR	dataset
Assign	User	1	the	Contributor	role	for	Workspace	B
You	have	a	Power	BI	workspace	named	BI	Data	that	contains	a	dataset	named	BI	Finance.
You	have	the	Build	permission	for	the	BI	Finance	dataset,	but	you	do	NOT	have	permissions	for	the	workspace.
You	need	to	connect	to	BI	Finance	and	create	a	report.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

---

## Question 268
**Énoncé de la question :**
Grant	User	1	the	Build	Permission	for	the	HR	dataset
Assign	User	1	the	Contributor	role	for	Workspace	B
You	have	a	Power	BI	workspace	named	BI	Data	that	contains	a	dataset	named	BI	Finance.
You	have	the	Build	permission	for	the	BI	Finance	dataset,	but	you	do	NOT	have	permissions	for	the	workspace.
You	need	to	connect	to	BI	Finance	and	create	a	report.
Which	two	actions	should	you	perform?	Each	correct	answer	presents	a	complete	solution.
NOTE:	Each	correct	selection	is	worth	one	point.

**Réponse exacte :**
CD

**Explication courte :**
The	answer	is	correct	:	CD	From	the	Power	BI	service,	create	a	new	report	and	select	a	published	dataset.From
Power	BI	Desktop,	connect	to	a	shared	dataset.
You	publish	a	dataset	to	the	Power	BI	service.	The	dataset	contains	a	connection	to	an	on-premises	Microsoft	SQL
Server	database.
You	attempt	to	configure	a	scheduled	refresh	but	cannot	select	the	appropriate	on-premises	data	gateway.
You	confirm	the	following	with	the	administrator	of	the	gateway:
•You	have	the	appropriate	permissions	to	use	the	gateway.
•The	data	source	was	created	on	the	gateway.
•The	gateway	has	a	status	of	Running.
What	is	the	most	likely	reason	the	gateway	is	unavailable?
A.
The	type	of	data	source	is	not	supported	by	the	on-premises	data	gateway.
B.
The	server	name	in	the	PBIX	file	does	not	match	the	data	source	name	in	the	gateway.
C.
The	credentials	for	the	data	source	are	invalid.
D.
The	data	source	is	configured	to	use	single	sign-on	(SSO).
Answer:	
B
Explanation:
In	Power	BI,	when	you	configure	a	data	source	to	use	an	on-premises	data	gateway,	the	server	name	and	other
connection	details	in	your	PBIX	file	must	match	the	data	source	configuration	in	the	gateway.	If	there's	a
mismatch	in	the	server	name	or	other	connection	details,	the	scheduled	refresh	won't	work,	and	you	won't	be
able	to	select	the	appropriate	gateway.
You	create	a	report	by	using	Microsoft	Power	BI	Desktop.
The	report	uses	data	from	a	Microsoft	SQL	Server	Analysis	Services	(SSAS)	tabular	model	located	on	your
company's	internal	network.
You	plan	to	publish	the	report	to	the	Power	BI	Service.
What	should	you	implement	to	ensure	that	users	who	consume	the	report	from	the	Power	BI	Service	have	the	most
up-to-date	data	from	the	tabular	model?
A.
a	scheduled	refresh	of	the	semantic	model

---

## Question 270
**Énoncé de la question :**
The	answer	is	correct	:	CD	From	the	Power	BI	service,	create	a	new	report	and	select	a	published	dataset.From
Power	BI	Desktop,	connect	to	a	shared	dataset.
You	publish	a	dataset	to	the	Power	BI	service.	The	dataset	contains	a	connection	to	an	on-premises	Microsoft	SQL
Server	database.
You	attempt	to	configure	a	scheduled	refresh	but	cannot	select	the	appropriate	on-premises	data	gateway.
You	confirm	the	following	with	the	administrator	of	the	gateway:
•You	have	the	appropriate	permissions	to	use	the	gateway.
•The	data	source	was	created	on	the	gateway.
•The	gateway	has	a	status	of	Running.
What	is	the	most	likely	reason	the	gateway	is	unavailable?
A.
The	type	of	data	source	is	not	supported	by	the	on-premises	data	gateway.
B.
The	server	name	in	the	PBIX	file	does	not	match	the	data	source	name	in	the	gateway.
C.
The	credentials	for	the	data	source	are	invalid.
D.
The	data	source	is	configured	to	use	single	sign-on	(SSO).
Answer:	
B
Explanation:
In	Power	BI,	when	you	configure	a	data	source	to	use	an	on-premises	data	gateway,	the	server	name	and	other
connection	details	in	your	PBIX	file	must	match	the	data	source	configuration	in	the	gateway.	If	there's	a
mismatch	in	the	server	name	or	other	connection	details,	the	scheduled	refresh	won't	work,	and	you	won't	be
able	to	select	the	appropriate	gateway.
You	create	a	report	by	using	Microsoft	Power	BI	Desktop.
The	report	uses	data	from	a	Microsoft	SQL	Server	Analysis	Services	(SSAS)	tabular	model	located	on	your
company's	internal	network.
You	plan	to	publish	the	report	to	the	Power	BI	Service.
What	should	you	implement	to	ensure	that	users	who	consume	the	report	from	the	Power	BI	Service	have	the	most
up-to-date	data	from	the	tabular	model?
A.
a	scheduled	refresh	of	the	semantic	model

**Réponse exacte :**
C

**Explication courte :**
an	On-premises	data	gateway.

---

## Question 272
**Énoncé de la question :**
an	On-premises	data	gateway.
HOTSPOT
-
You	have	a	semantic	model	that	has	the	permissions	shown	in	the	following	exhibit.
Use	the	drop-down	menus	to	select	the	answer	choice	that	completes	each	statement	based	on	the	information
presented	in	the	graphic.
NOTE:	Each	correct	selection	is	worth	one	point.
Answer:

**Réponse exacte :**
A

**Explication courte :**
Executives	require	a	visual	that	shows	sales	by	region.
The	data	type	of	Sales[region_id]	must	be	changed	from	varchar	to	Whole	Number,	as	Sales[region_id]	is
Integer.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Litware,	Inc.	is	an	online	retailer	that	uses	Power	BI.
Litware	plans	to	leverage	data	from	an	Azure	SQL	database	that	stores	data	for	the	company's	live	e-commerce
website.
Litware	uses	Azure	Active	Directory	(Azure	AD)	to	authenticate	users.
Existing	Environment.	Sales	Data
Litware	has	online	sales	data	that	has	the	SQL	schema	shown	in	the	following	table.

---

## Question 273
**Énoncé de la question :**
Executives	require	a	visual	that	shows	sales	by	region.
The	data	type	of	Sales[region_id]	must	be	changed	from	varchar	to	Whole	Number,	as	Sales[region_id]	is
Integer.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Litware,	Inc.	is	an	online	retailer	that	uses	Power	BI.
Litware	plans	to	leverage	data	from	an	Azure	SQL	database	that	stores	data	for	the	company's	live	e-commerce
website.
Litware	uses	Azure	Active	Directory	(Azure	AD)	to	authenticate	users.
Existing	Environment.	Sales	Data
Litware	has	online	sales	data	that	has	the	SQL	schema	shown	in	the	following	table.

**Réponse exacte :**
C

**Explication courte :**
C.	DirectQuery	that	uses	a	database	credential
If	you	used	the	credentials	of	the	user	(D)	then	all	users	would	need	to	be	created	in	the	database.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the

---

## Question 274
**Énoncé de la question :**
C.	DirectQuery	that	uses	a	database	credential
If	you	used	the	credentials	of	the	user	(D)	then	all	users	would	need	to	be	created	in	the	database.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the

**Réponse exacte :**
A

**Explication courte :**
You	wouldn't	use	composite	for	all.	I	would	say	import	as	the	SQL	Server	data	is	only	2GB	and	excel	is	really
small.	Also,	only	need	it	refreshing	once	a	day	so	this	dataset	is	very	small.	Answer	is	A	(Import)
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the
following	table.

---

## Question 275
**Énoncé de la question :**
You	wouldn't	use	composite	for	all.	I	would	say	import	as	the	SQL	Server	data	is	only	2GB	and	excel	is	really
small.	Also,	only	need	it	refreshing	once	a	day	so	this	dataset	is	very	small.	Answer	is	A	(Import)
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the
following	table.

**Réponse exacte :**
D

**Explication courte :**
D	-	Add	the	sales	department	as	a	member	of	the	reports	workspace.
For	the	actions	they	need	to	perform	(edit	reports,	publish	app,	etc)	the	Member	role	would	be	the	least
privilege
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the
following	table.

---

## Question 276
**Énoncé de la question :**
D	-	Add	the	sales	department	as	a	member	of	the	reports	workspace.
For	the	actions	they	need	to	perform	(edit	reports,	publish	app,	etc)	the	Member	role	would	be	the	least
privilege
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
General	Overview	-
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Business	Issues	-
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting	Services
(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the	report
requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.	The	first	11	rows	of	the	worksheet	are	shown	in	the
following	table.

**Réponse exacte :**


**Explication courte :**
Box	1:	
dashboard	-
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
You	can	set	alerts	to	notify	you	when	data	in	your	dashboards	changes	beyond	limits	you	set.
Box	2:	
data	alert	-
Reference:
https://docs.microsoft.com/en-us/power-bi/create-reports/service-set-data-alerts
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage

---

## Question 277
**Énoncé de la question :**
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage

**Réponse exacte :**
D

**Explication courte :**
One	product	in	the	product	list	can	occur	many	times	in	the	revenue	results.
Note	1:	One	to	many	(1:*):	In	a	one-to-many	relationship,	the	column	in	one	table	has	only	one	instance	of	a
particular	value,	and	the	other	related	table	can	have	more	than	one	instance	of	a	value.
Note	2:
Revenue	data	is	provided	at	the	date	and	product	level.
The	board	must	be	able	to	get	the	following	information	from	the	quarterly	reports:
Revenue	trends	over	time	-
The	percent	of	total	revenue	contributed	by	each	product	category
A	comparison	of	quarterly	revenue	versus	the	same	quarter	from	the	previous	year
Reference:
https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-create-and-manage-relationships
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.

---

## Question 278
**Énoncé de la question :**
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.

**Réponse exacte :**


**Explication courte :**
Box	1:	CALCULATE	-
CALCULATE	evaluates	an	expression	in	a	modified	filter	context.
Syntax:	CALCULATE(<expression>[,	<filter1>	[,	<filter2>	[,	
�
]]])
Box	2:	ALL-
Box	3:	DIVIDE	-
DIVIDE	performs	a	division.
Example:	MEASURE	FactInternetSales[%Sales]	=	DIVIDE([TotalSales],
CALCULATE([TotalSales],REMOVEFILTERS()))
Note:	The	RETURN	keyword	consumes	variables	defined	in	previous	VAR	statements.
VAR	AllCategoryRev	=
CALCULATE
(SUM([Revenue]),
ALL
(ProductList[ProductCategory]))
RETURN
DIVIDE
(SUM([Revenue]),	AllCategoryRev
Anyone	with	experience	in	DAX	would	only	need	to	read	the	question	in	these	case	study	questions.	The
questions	seem	to	hint	the	answer	already..	for	this	question	for	example	anyone	would	know	that	the	moment
you	see	a	percentage	of	the	total	is	required	you	would	immediately	go	with	the	ALL	function	and	the	rest	is
easy.
Reference:
https://docs.microsoft.com/en-us/dax/calculate-function-dax
https://docs.microsoft.com/en-us/dax/removefilters-function-dax	https://dax.guide/st/return/
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such

---

## Question 279
**Énoncé de la question :**
https://docs.microsoft.com/en-us/dax/removefilters-function-dax	https://dax.guide/st/return/
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such

**Réponse exacte :**


**Explication courte :**
1)	Create	four	roles
2)	add	DAX	filters
3)	publish
4)	add	role	members
Contributor	role	give	analysts	a	possibility	to	save	reports	to	a	workspace,	which	is	not	permitted	by
requirements
Reference:
https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls
Introductory	Info
	Case	Study	-

---

## Question 280
**Énoncé de la question :**
Introductory	Info
	Case	Study	-

**Réponse exacte :**
A

**Explication courte :**
A)	-	LASTDATE()
as	we	do	not	sum	the	balances	of	last	3	months
The	board	meeting	requires	quarter	balance.	For	example,	Jan	-	Mar.	So	what	we	need	is	the	balance	as	at	31
Mar,	the	LASTDATE	is	appropriate.	The	balance	sheet	already	gives	you	the	number	directly.	No	need	to
calculate	up	to	3	months.
In	case	of	using	DATESQTD,	daily	sale	and	expenses	will	be	listed	in	a	table	rather	than	balance	in	balance
sheet.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an

---

## Question 281
**Énoncé de la question :**
A)	-	LASTDATE()
as	we	do	not	sum	the	balances	of	last	3	months
The	board	meeting	requires	quarter	balance.	For	example,	Jan	-	Mar.	So	what	we	need	is	the	balance	as	at	31
Mar,	the	LASTDATE	is	appropriate.	The	balance	sheet	already	gives	you	the	number	directly.	No	need	to
calculate	up	to	3	months.
In	case	of	using	DATESQTD,	daily	sale	and	expenses	will	be	listed	in	a	table	rather	than	balance	in	balance
sheet.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an

**Réponse exacte :**
D

**Explication courte :**
Two	date	dims,	two	1:*	relationships
The	customer	service	department	requires	a	visual	that	can	be	filtered	by	both	sales	month	and	ship	month
independently.
Need	two	date	tables.	Add	a	one-to-many	relationship	from	both	the	Date	tables	to	Sales	table.
Reference:
https://docs.microsoft.com/en-us/power-bi/guidance/relationships-active-inactive
You	need	to	provide	a	solution	to	provide	the	sales	managers	with	the	required	access.
What	should	you	include	in	the	solution?
A.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales	Manager	table	where	username	=	UserName().
B.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales	Manager	table	where	username	=	sales_manager_id.
C.	
Create	a	security	role	that	has	a	table	filter	on	the	Region	Manager	table	where	sales_manager_id	=
UserPrincipalName().
D.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales_Manager	table	where	name	=	UserName().
Answer:	
A
Explanation:

---

## Question 282
**Énoncé de la question :**
You	need	to	provide	a	solution	to	provide	the	sales	managers	with	the	required	access.
What	should	you	include	in	the	solution?
A.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales	Manager	table	where	username	=	UserName().
B.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales	Manager	table	where	username	=	sales_manager_id.
C.	
Create	a	security	role	that	has	a	table	filter	on	the	Region	Manager	table	where	sales_manager_id	=
UserPrincipalName().
D.	
Create	a	security	role	that	has	a	table	filter	on	the	Sales_Manager	table	where	name	=	UserName().
Answer:	
A
Explanation:

**Réponse exacte :**
D

**Explication courte :**
D	seems	to	be	correct	because	the	Executives	will	only	be	able	to	see	Region	managers	and	Sales	managers
that	report	to	them	in	a	hierarchy,	besides	there	is	nothing	to	measure	there	so	A	is	actually	wrong
Executives	require	a	visual	that	shows	returns	by	region	manager	and	the	sales	managers	that	report	to	them.
A	hierarchy	is	a	set	of	fields	categorized	in	a	hierarchical	way	that	one	level	is	the	parent	of	another	level.
Values	of	the	parent	level	can	be	drilled	down	to	the	lower	level.
Reference:
https://radacad.com/what-a-power-bi-hierarchy-is-and-how-to-use-it
______________________________________________________________________________
Case	Study	Description
Litware,	Inc.	Case	Study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like
to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must
manage	your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time
provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about
the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this
case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and
to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot

---

## Question 283
**Énoncé de la question :**
______________________________________________________________________________
Case	Study	Description
Litware,	Inc.	Case	Study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like
to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must
manage	your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time
provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about
the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this
case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and
to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot

**Réponse exacte :**
A

**Explication courte :**
The	sales	department	requires	reports	that	contain	the	number	of	sales	transactions.
The	COUNTROWS	function	counts	the	number	of	rows	in	the	specified	table,	or	in	a	table	defined	by	an
expression.
Incorrect:
The	COUNTA	function	counts	the	number	of	cells	in	a	column	that	are	not	empty.
Reference:

---

## Question 284
**Énoncé de la question :**
The	sales	department	requires	reports	that	contain	the	number	of	sales	transactions.
The	COUNTROWS	function	counts	the	number	of	rows	in	the	specified	table,	or	in	a	table	defined	by	an
expression.
Incorrect:
The	COUNTA	function	counts	the	number	of	cells	in	a	column	that	are	not	empty.
Reference:

**Réponse exacte :**
B

**Explication courte :**
You	are	concerned	with	the	quality	and	completeness	of	the	sales	data.	You	must	ensure	that	negative	and
missing	sales_amount	values	do	NOT	contribute	to	the	total	sales	amount	calculation.
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information

---

## Question 285
**Énoncé de la question :**
You	are	concerned	with	the	quality	and	completeness	of	the	sales	data.	You	must	ensure	that	negative	and
missing	sales_amount	values	do	NOT	contribute	to	the	total	sales	amount	calculation.
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information

**Réponse exacte :**
A

**Explication courte :**
Users	must	be	able	to	see	the	month	in	each	report	as	shown	in	the	following	example:	Feb	2020.
Custom	date/time	formats	-
The	following	format	characters	can	be	specified	in	the	format_string	to	create	custom	date/time	formats:
*	mmm
Display	the	month	as	an	abbreviation	(Jan-Dec).	Localized.

---

## Question 286
**Énoncé de la question :**
Users	must	be	able	to	see	the	month	in	each	report	as	shown	in	the	following	example:	Feb	2020.
Custom	date/time	formats	-
The	following	format	characters	can	be	specified	in	the	format_string	to	create	custom	date/time	formats:
*	mmm
Display	the	month	as	an	abbreviation	(Jan-Dec).	Localized.

**Réponse exacte :**


**Explication courte :**
Box	1:
	No-
Customer	ID	in	Orders	is	text	("VINET")	while	Customer	ID	in	Customer	Details	is	number	("1").
Box	2:
	Yes-
Relationship	between	Orders	and	Customer	Details	will	be	via	column	Customer	CRMID	in	Customer	Details
and	Customer	ID	in	Orders,	which	are	both	text.
Box	3:
	No	-
the	Orders	table	only	contains	shipping	address,	which	is	different	from	the	billing	address	which	should	be
used	for	sales	region.	Thus,	it	should	come	from	Customer	Details	table.
No	-	Yes	-	No.	According	to	the	sample	data	the	Customer	ID	in	Customer	Details	is	a	number	(1	through	10	is
shown	in	the	example	data)	and	the	Customer	ID	in	the	Orders	table	has	an	example	value	of	VINET,	which
looks	like	it	corresponds	to	the	value	of	Customer	CRMID	instead	of	Customer	ID	from	the	Customer	Details
worksheet	so	the	first	answer	should	be	No.	The	second	answer	should	be	Yes,	the	Customer	ID	from	Orders
has	example	value	VINET,	which	is	text.
___________________________________________________________________________

---

## Question 288
**Énoncé de la question :**
Box	1:
	No-
Customer	ID	in	Orders	is	text	("VINET")	while	Customer	ID	in	Customer	Details	is	number	("1").
Box	2:
	Yes-
Relationship	between	Orders	and	Customer	Details	will	be	via	column	Customer	CRMID	in	Customer	Details
and	Customer	ID	in	Orders,	which	are	both	text.
Box	3:
	No	-
the	Orders	table	only	contains	shipping	address,	which	is	different	from	the	billing	address	which	should	be
used	for	sales	region.	Thus,	it	should	come	from	Customer	Details	table.
No	-	Yes	-	No.	According	to	the	sample	data	the	Customer	ID	in	Customer	Details	is	a	number	(1	through	10	is
shown	in	the	example	data)	and	the	Customer	ID	in	the	Orders	table	has	an	example	value	of	VINET,	which
looks	like	it	corresponds	to	the	value	of	Customer	CRMID	instead	of	Customer	ID	from	the	Customer	Details
worksheet	so	the	first	answer	should	be	No.	The	second	answer	should	be	Yes,	the	Customer	ID	from	Orders
has	example	value	VINET,	which	is	text.
___________________________________________________________________________

**Réponse exacte :**


**Explication courte :**
Box	1:	
CALCULATE	-
CALCULATE	evaluates	an	expression	in	a	modified	filter	context.
Syntax:	CALCULATE(<expression>[,	<filter1>	[,	<filter2>	[,	¦]]])	expression	-	The	expression	to	be	evaluated.
filter1,	filter2,..	-	(Optional)	Boolean	expressions	or	table	expressions	that	defines	filters,	or	filter	modifier
functions.
Incorrect:
*	COUNTX	-	Counts	the	number	of	rows	that	contain	a	non-blank	value	or	an	expression	that	evaluates	to	a
non-blank	value,	when	evaluating	an	expression	over	a	table.
*	CALCULATETABLE	evaluates	a	table	expression	in	a	modified	filter	context.
Syntax:	CALCULATETABLE(<expression>[,	<filter1>	[,	<filter2>	[,	¦]]])
Expression	-	The	table	expression	to	be	evaluated.
Box	2:	
FILTER	-
FILTER	returns	a	table	that	represents	a	subset	of	another	table	or	expression.
Syntax:	FILTER(<table>,<filter>)
Box	3:	
Orders[Shipped	Date]	>	Orders[Required	Date]
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
Reference:
https://docs.microsoft.com/en-us/dax/calculate-function-dax
https://docs.microsoft.com/en-us/dax/filter-function-dax
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	minimize	the	size	of	the	dataset.	The	solution	must	meet	the	report	requirements.
What	should	you	do?
A.	
Group	the	Categories	table	by	the	CategoryID	column.
B.	
Remove	the	QuantityPerUnit	column	from	the	Products	table.
C.	
Filter	out	discontinued	products	while	importing	the	Products	table.
D.	
Change	the	OrderID	column	in	the	Orders	table	to	the	Text	data	type.
Answer:	
B
Explanation:
Removing	a	column	which	isn't	used	in	the	reports	reduces	the	dataset	size.
Incorrect:
Not	A:	Grouping	does	not	affect	size.
Not	C:	Cannot	filter	out	discontinued	products	as:	The	reports	must	show	historical	data	for	the	current
calendar	year	and	the	last	three	calendar	years.

---

## Question 289
**Énoncé de la question :**
https://docs.microsoft.com/en-us/dax/filter-function-dax
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	minimize	the	size	of	the	dataset.	The	solution	must	meet	the	report	requirements.
What	should	you	do?
A.	
Group	the	Categories	table	by	the	CategoryID	column.
B.	
Remove	the	QuantityPerUnit	column	from	the	Products	table.
C.	
Filter	out	discontinued	products	while	importing	the	Products	table.
D.	
Change	the	OrderID	column	in	the	Orders	table	to	the	Text	data	type.
Answer:	
B
Explanation:
Removing	a	column	which	isn't	used	in	the	reports	reduces	the	dataset	size.
Incorrect:
Not	A:	Grouping	does	not	affect	size.
Not	C:	Cannot	filter	out	discontinued	products	as:	The	reports	must	show	historical	data	for	the	current
calendar	year	and	the	last	three	calendar	years.

**Réponse exacte :**
A

**Explication courte :**
Because	we	do	have	visuals	that	need	a	filter	on	either	order	or	shipping	date,	but	no	visual	requires	a	filter	on
both	at	the	same	time.
Auto	date/time	does	not	meet	the	criteria:	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as
possible,	while	meeting	the	report	requirements	and	the	technical	requirements.

---

## Question 291
**Énoncé de la question :**
Because	we	do	have	visuals	that	need	a	filter	on	either	order	or	shipping	date,	but	no	visual	requires	a	filter	on
both	at	the	same	time.
Auto	date/time	does	not	meet	the	criteria:	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as
possible,	while	meeting	the	report	requirements	and	the	technical	requirements.

**Réponse exacte :**


**Explication courte :**
Box	1:	many-to-many	-
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
With	composite	models,	you	can	establish	a	many-to-many	relationship	between	tables,	which	removes
requirements	for	unique	values	in	tables.	It	also	removes	previous	workarounds,	such	as	introducing	new
tables	only	to	establish	relationships.
Box	2:	
Customer	details
Sales	employees	should	see	the	sales	of	their	region	only,	so	all	sales	ordered	by	customers	whose	billing
address	belongs	to	the	sales	employee's	region.
Therefore,	the	relationship	between	sales	employees	(region)	and	customer	details	(region)	should	be	many-
to-many	(a	sales	employee	has	many	customers	in	his	region	and	a	customer	in	a	region	can	have	many	sales
employees	for	that	region).
In	this	case,	as	the	customer	table	is	related	to	the	order	table,	the	sales	employees	will	only	be	able	to	see
the	orders	of	the	customers	in	their	region.
Reference:
https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-create-and-manage-relationships
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	update	the	Power	BI	model	to	ensure	that	the	analysts	can	quickly	build	drill-downs	from	business
unit	to	product	in	a	visual.
What	should	you	create?
A.	
a	group
B.	
a	calculated	table
C.	
a	hierarchy
D.	
a	calculated	column
Answer:	
C
Explanation:
Drill	requires	a	hierarchy.
When	a	visual	has	a	hierarchy,	you	can	drill	down	to	reveal	additional	details.
Reference:
https://docs.microsoft.com/en-us/power-bi/consumer/end-user-drill

---

## Question 293
**Énoncé de la question :**
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	update	the	Power	BI	model	to	ensure	that	the	analysts	can	quickly	build	drill-downs	from	business
unit	to	product	in	a	visual.
What	should	you	create?
A.	
a	group
B.	
a	calculated	table
C.	
a	hierarchy
D.	
a	calculated	column
Answer:	
C
Explanation:
Drill	requires	a	hierarchy.
When	a	visual	has	a	hierarchy,	you	can	drill	down	to	reveal	additional	details.
Reference:
https://docs.microsoft.com/en-us/power-bi/consumer/end-user-drill

**Réponse exacte :**


**Explication courte :**
Box	1:	
Top	N	-
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
Box	2:	
Visual	-
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Applying	specific	measures	to	the	visual-level	filter	of	a	visualization	is	a	very	powerful	technique	to
completely	customize	the	items	shown	in	a	report.	The	presence	of	this	filter	requires	special	measures	in
order	to	display	values	related	to	items	not	included	in	the	visual	level	filter.
Reference:
https://www.sqlbi.com/articles/filtering-the-top-3-products-for-each-category-in-power-bi/
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	create	the	On-Time	Shipping	report.	The	report	must	include	a	visualization	that	shows	the	percentage

---

## Question 294
**Énoncé de la question :**
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
You	need	to	create	the	On-Time	Shipping	report.	The	report	must	include	a	visualization	that	shows	the	percentage

**Réponse exacte :**
C

**Explication courte :**
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
Bar	and	column	charts	are	some	of	the	most	widely	used	visualization	charts	in	Power	BI.	They	can	be	used	for
one	or	multiple	categories.	Both	these	chart	types	represent	data	with	rectangular	bars,	where	the	size	of	the
bar	is	proportional	to	the	magnitude	of	data	values.
Reference:
https://www.pluralsight.com/guides/bar-and-column-charts-in-power-bi
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.

---

## Question 295
**Énoncé de la question :**
___________________________________________________________________________
Case	Study	Description
Northwind	Traders
Case	study
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would
like	to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You
must	manage	your	time	to	ensure	that	you	are	able	to	complete	all	question	included	on	this	exam	in	the
time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information
about	the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	question
on	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers
and	to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you
cannot	return	to	this	section.
To	start	the	case	study
To	display	the	first	question	on	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment,	and	problem	statements.	If	the	case
study	has	an	All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information
displayed	on	the	subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to
return	to	the	question.
Overview.
General	Overview
Northwind	Traders	is	a	specialty	food	import	company.
The	company	recently	implemented	Power	BI	to	better	understand	its	top	customers,	products,	and	suppliers.
Overview.	Business	Issues
The	sales	department	relies	on	the	IT	department	to	generate	reports	in	Microsoft	SQL	Server	Reporting
Services	(SSRS).	The	IT	department	takes	too	long	to	generate	the	reports	and	often	misunderstands	the
report	requirements.
Existing	Environment.	Data	Sources
Northwind	Traders	uses	the	data	sources	shown	in	the	following	table.
Source2	is	exported	daily	from	a	third-party	system	and	stored	in	Microsoft	SharePoint	Online.
Existing	Environment.	Customer	Worksheet
Source2	contains	a	single	worksheet	named	Customer	Details.
The	first	11	rows	of	the	worksheet	are	shown	in	the	following	table.
All	the	fields	in	Source2	are	mandatory.
The	Address	column	in	Customer	Details	is	the	billing	address,	which	can	differ	from	the	shipping	address.
Existing	Environment.	Azure	SQL	Database
Source1	contains	the	following	table:
-	Orders
-	Products
-	Suppliers
-	Categories
-	Order	Details
-	Sales	Employees
The	Orders	table	contains	the	following	columns.
The	Order	Details	table	contains	the	following	columns.
The	address	in	the	Orders	table	is	the	shipping	address,	which	can	differ	from	the	billing	address.
The	Products	table	contains	the	following	columns.
The	Categories	table	contains	the	following	columns.
The	Suppliers	table	contains	the	following	columns.
The	Sales	Employees	table	contains	the	following	columns.
Each	employee	in	the	Sales	Employees	table	is	assigned	to	one	sales	region.	Multiple	employees	can	be
assigned	to	each	region.
Requirements.
Report	Requirements
Northwind	Traders	requires	the	following	reports:
-	Top	Products
-	Top	Customers
-	On-Time	Shipping
The	Top	Customers	report	will	show	the	top	20	customers	based	on	the	highest	sales	amounts	in	a	selected
order	month	or	quarter,	product	category,	and	sales	region.
The	Top	Products	report	will	show	the	top	20	products	based	on	the	highest	sales	amounts	sold	in	a	selected
order	month	or	quarter,	sales	region,	and	product	category.	The	report	must	also	show	which	suppliers
provide	the	top	products.
The	On-Time	Shipping	report	will	show	the	following	metrics	for	a	selected	shipping	month	or	quarter:
-	The	percentage	of	orders	that	were	shipped	late	by	country	and	shipping	region
-	Customers	that	had	multiple	late	shipments	during	the	last	quarter
Northwind	Traders	defines	late	orders	as	those	shipped	after	the	required	shipping	date.
The	warehouse	shipping	department	must	be	notified	if	the	percentage	of	late	orders	within	the	current
month	exceeds	5%.
The	reports	must	show	historical	data	for	the	current	calendar	year	and	the	last	three	calendar	years.
Requirements.	Technical	Requirements
Northwind	Traders	identifies	the	following	technical	requirements:
-	A	single	dataset	must	support	all	three	reports.
-	The	reports	must	be	stored	in	a	single	Power	BI	workspace.
-	Report	data	must	be	current	as	of	7	AM	Pacific	Time	each	day.
-	The	reports	must	provide	fast	response	times	when	users	interact	with	a	visualization.
-	The	data	model	must	minimize	the	size	of	the	dataset	as	much	as	possible,	while	meeting	the	report
requirements	and	the	technical	requirements.
Requirements.
Security	Requirements
Access	to	the	reports	must	be	granted	to	Azure	Active	Directory	(Azure	AD)	security	groups	only.
An	Azure	AD	security	group	exists	for	each	department.
The	sales	department	must	be	able	to	perform	the	following	tasks	in	Power	BI:
-	Create,	edit,	and	delete	content	in	the	reports.
-	Manage	permissions	for	workspaces,	datasets,	and	report.
-	Publish,	unpublish,	update,	and	change	the	permissions	for	an	app.
-	Assign	Azure	AD	groups	role-based	access	to	the	reports	workspace.
Users	in	the	sales	department	must	be	able	to	access	only	the	data	of	the	sales	region	to	which	they	are
assigned	in	the	Sales	Employees	table.
Power	BI	has	the	following	row-level	security	(RLS)	Table	filter	DAX	expression	for	the	Sales	Employees
table.
[EmailAddress]	=	USERNAME()
RLS	will	be	applied	only	to	the	sales	department	users.	Users	in	all	other	departments	must	be	able	to	view	all
the	data.
HOTSPOT	-
You	need	to	create	a	KPI	visualization	to	meet	the	reporting	requirements	of	the	sales	managers.
How	should	you	create	the	visualization?	To	answer,	select	the	appropriate	options	in	the	answer	area.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:

**Réponse exacte :**


**Explication courte :**
The	sales	managers	require	a	visual	to	analyze	sales	performance	versus	sales	targets.
Box	1:	Sales[sales_amount]
Value;	The	main	measure	which	we	want	to	evaluate
Example:
Sales	=	sum(FactInternetSales[SalesAmount])
Box	2:	Date[month]
Trend;	How	Value	perfoms	in	a	time	period,	is	it	going	upward,	downward¦?
You	can	use	Months	as	trend	axis.
Box	3:	Targets[sales_target]
Target;	What	we	want	to	compare	the	Value	with
Reference:
https://radacad.com/kpi-visual-in-power-bi-explained
_________________________________________________________________________
Case	Study	Description
Introductory	Info
Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like
to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must
manage	your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time
provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about
the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this
case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and
to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot
return	to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study
has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the
subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the
question.
Overview	-
Litware,	Inc.	is	an	online	retailer	that	uses	Power	BI.
Litware	plans	to	leverage	data	from	an	Azure	SQL	database	that	stores	data	for	the	company's	live	e-
commerce	website.
Litware	uses	Azure	Active	Directory	(Azure	AD)	to	authenticate	users.
Existing	Environment.	Sales	Data
Litware	has	online	sales	data	that	has	the	SQL	schema	shown	in	the	following	table.
In	the	Date	table,	the	date_id	column	has	a	format	of	yyyymmdd	and	the	month	column	has	a	format	of
yyyymm.
The	week	column	in	the	Date	table	and	the	week_id	column	in	the	Weekly_Returns	table	have	a	format	of
yyyyww.
In	the	Sales	table,	the	sales_id	column	represents	a	unique	transaction.
The	region	id	column	can	be	managed	by	only	one	sales	manager.
Existing	Environment.	Data	Concerns
You	are	concerned	with	the	quality	and	completeness	of	the	sales	data.	You	must	ensure	that	negative	and
missing	sales_amount	values	do	NOT	contribute	to	the	total	sales	amount	calculation.
Existing	Environment.	Reporting	Requirements
Litware	identifies	the	following	reporting	requirements:
Executives	require	a	visual	that	shows	sales	by	region.
Executives	require	a	visual	that	shows	returns	by	region	manager	and	the	sales	managers	that	report	to	them.
The	sales	managers	must	be	able	to	see	only	the	sales	data	of	their	respective	region.
The	sales	managers	require	a	visual	to	analyze	sales	performance	versus	sales	targets.
The	sales	department	requires	reports	that	contain	the	number	of	sales	transactions.
Users	must	be	able	to	see	the	month	in	each	report	as	shown	in	the	following	example:	Feb	2020.
The	customer	service	department	requires	a	visual	that	can	be	filtered	by	both	sales	month	and	ship	month
independently.
The	maximum	allowed	latency	to	include	transactions	in	reports	is	five	minutes.

---

## Question 297
**Énoncé de la question :**
_________________________________________________________________________
Case	Study	Description
Introductory	Info
Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like
to	complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must
manage	your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time
provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in
the	case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about
the	scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this
case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and
to	make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot
return	to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to
explore	the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays
information	such	as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study
has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the
subsequent	tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the
question.
Overview	-
Litware,	Inc.	is	an	online	retailer	that	uses	Power	BI.
Litware	plans	to	leverage	data	from	an	Azure	SQL	database	that	stores	data	for	the	company's	live	e-
commerce	website.
Litware	uses	Azure	Active	Directory	(Azure	AD)	to	authenticate	users.
Existing	Environment.	Sales	Data
Litware	has	online	sales	data	that	has	the	SQL	schema	shown	in	the	following	table.
In	the	Date	table,	the	date_id	column	has	a	format	of	yyyymmdd	and	the	month	column	has	a	format	of
yyyymm.
The	week	column	in	the	Date	table	and	the	week_id	column	in	the	Weekly_Returns	table	have	a	format	of
yyyyww.
In	the	Sales	table,	the	sales_id	column	represents	a	unique	transaction.
The	region	id	column	can	be	managed	by	only	one	sales	manager.
Existing	Environment.	Data	Concerns
You	are	concerned	with	the	quality	and	completeness	of	the	sales	data.	You	must	ensure	that	negative	and
missing	sales_amount	values	do	NOT	contribute	to	the	total	sales	amount	calculation.
Existing	Environment.	Reporting	Requirements
Litware	identifies	the	following	reporting	requirements:
Executives	require	a	visual	that	shows	sales	by	region.
Executives	require	a	visual	that	shows	returns	by	region	manager	and	the	sales	managers	that	report	to	them.
The	sales	managers	must	be	able	to	see	only	the	sales	data	of	their	respective	region.
The	sales	managers	require	a	visual	to	analyze	sales	performance	versus	sales	targets.
The	sales	department	requires	reports	that	contain	the	number	of	sales	transactions.
Users	must	be	able	to	see	the	month	in	each	report	as	shown	in	the	following	example:	Feb	2020.
The	customer	service	department	requires	a	visual	that	can	be	filtered	by	both	sales	month	and	ship	month
independently.
The	maximum	allowed	latency	to	include	transactions	in	reports	is	five	minutes.
HOTSPOT	-
You	publish	the	dataset	to	powerbi.com.
For	each	of	the	following	statements,	select	Yes	if	the	statement	is	true.	Otherwise,	select	No.
NOTE:	Each	correct	selection	is	worth	one	point.
Hot	Area:
Answer:
Explanation:
No
Azure	SQL	Server,	therefore	no	need	for	an	on-premise	Gateway	as	Service	and	Azure	are	in	the	cloud.
No
Direct	Query	mode	for	the	DB	connection,	so	no	need	to	schedule	a	refresh.	Direct	Query	is	a	live	connection.
No
Azure	SQL	supports	the	following	connections	from	Power	BI:	Windows,	Database	and	Microsoft	Account.
(Basic	is	reserved	for	Power	Query	Online.	Do	not	confuse	Database	with	Basic.):
https://learn.microsoft.com/en-us/power-query/connectors/azuresqldatabase

**Réponse exacte :**
C

**Explication courte :**
a	calculated	column	that	uses	the	following	formula:	IF(ISBLANK(Sales[sales_amount]),0,
(Sales[sales_amount]))
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Contoso,	Ltd.	is	a	manufacturing	company	that	produces	sports	equipment.	Contoso	holds	quarterly	board
meetings	for	which	financial	analysts	manually	prepare
Microsoft	Excel	reports,	including	balance	sheets	and	profit	and	loss	statements	for	each	of	the	company's	four
business	units.
Existing	Environment	-
Data	and	Sources	-
Data	for	the	reports	comes	from	the	sources	shown	in	the	following	table.
The	balance	sheet	data	is	unrelated	to	the	profit	and	loss	results	other	than	they	both	relate	to	dates.

---

## Question 298
**Énoncé de la question :**
a	calculated	column	that	uses	the	following	formula:	IF(ISBLANK(Sales[sales_amount]),0,
(Sales[sales_amount]))
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Contoso,	Ltd.	is	a	manufacturing	company	that	produces	sports	equipment.	Contoso	holds	quarterly	board
meetings	for	which	financial	analysts	manually	prepare
Microsoft	Excel	reports,	including	balance	sheets	and	profit	and	loss	statements	for	each	of	the	company's	four
business	units.
Existing	Environment	-
Data	and	Sources	-
Data	for	the	reports	comes	from	the	sources	shown	in	the	following	table.
The	balance	sheet	data	is	unrelated	to	the	profit	and	loss	results	other	than	they	both	relate	to	dates.

**Réponse exacte :**


**Explication courte :**
Box	1:	The	Viewer	role	to	the	workspace
The	Viewer	role	gives	a	read-only	experience	to	its	users.	They	can	view	dashboards,	reports,	or	workbooks	in
the	workspace,	but	can't	browse	the	datasets	or	dataflows.	Use	the	Viewer	role	wherever	you	would
previously	use	a	classic	workspace	set	to	Members	can	only	view	Power	BI	content.
Box	2:	Build	-
The	analysts	must	be	able	to	build	new	reports	from	the	dataset	that	contains	the	profit	and	loss	data.
Scenario:	The	reports	must	be	made	available	to	the	board	from	powerbi.com.
The	analysts	responsible	for	each	business	unit	must	see	all	the	data	the	board	sees,	except	the	profit	and
loss	data,	which	must	be	restricted	to	only	their	business	unit's	data.	The	analysts	must	be	able	to	build	new
reports	from	the	dataset	that	contains	the	profit	and	loss	data,	but	any	reports	that	the	analysts	build	must
not	be	included	in	the	quarterly	reports	for	the	board.	The	analysts	must	not	be	able	to	share	the	quarterly
reports	with	anyone.
Reference:
https://www.nickyvv.com/2019/08/the-new-power-bi-workspace-viewer-role-explained.html
Deploy	and	Maintain	Deliverables
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.

---

## Question 299
**Énoncé de la question :**
Deploy	and	Maintain	Deliverables
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.

**Réponse exacte :**


**Explication courte :**
1.	Using	an	App
2.	A	mail-enabled	security	group	in	Azure	Active	Directory
Box	1:	Using	an	App
Box	2:	A	mail-enabled	security	group	in	Azure	Active	Directory
Mail-Enabled	Security	Group	-
This	group	also	contains	a	list	of	email	addresses	of	members	and	can	also	be	used	to	control	access	to
OneDrive	and	SharePoint.
The	Mail-Enabled	Security	Group	can	be	created	in	the	Office	365	Admin	Portal
Note:	The	reports	must	be	made	available	to	the	board	from	powerbi.com.	An	Azure	Active	Directory	(Azure
AD)	group	will	be	used	to	share	information	with	the	board.
Incorrect:
*	Distribution	Group
This	group	can	also	be	called	and	Distribution	List.	The	Distribution	Group	is	a	group	which	contains	a	list	of
email	addresses	of	members,	all	of	whom	will	be	sent	an	email	when	an	email	is	sent	to	the	distribution	groups
email	address.
The	Distribution	Group	can	be	created	in	the	Azure	Active	Directory
Reference:
https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-share-dashboards
https://www.fourmoo.com/2020/04/01/power-bi-which-groups-can-be-used-to-set-permissions-in-power-bi/
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Contoso,	Ltd.	is	a	manufacturing	company	that	produces	sports	equipment.	Contoso	holds	quarterly	board
meetings	for	which	financial	analysts	manually	prepare
Microsoft	Excel	reports,	including	balance	sheets	and	profit	and	loss	statements	for	each	of	the	company's	four
business	units.
Existing	Environment	-
Data	and	Sources	-
Data	for	the	reports	comes	from	the	sources	shown	in	the	following	table.
The	balance	sheet	data	is	unrelated	to	the	profit	and	loss	results	other	than	they	both	relate	to	dates.
Balance	Sheet	Data	-

---

## Question 300
**Énoncé de la question :**
https://www.fourmoo.com/2020/04/01/power-bi-which-groups-can-be-used-to-set-permissions-in-power-bi/
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the
case	study.	Case	studies	might	contain	exhibits	and	other	resources	that	provide	more	information	about	the
scenario	that	is	described	in	the	case	study.	Each	question	is	independent	of	the	other	questions	in	this	case	study.
At	the	end	of	this	case	study,	a	review	screen	will	appear.	This	screen	allows	you	to	review	your	answers	and	to
make	changes	before	you	move	to	the	next	section	of	the	exam.	After	you	begin	a	new	section,	you	cannot	return
to	this	section.
To	start	the	case	study	-
To	display	the	first	question	in	this	case	study,	click	the	Next	button.	Use	the	buttons	in	the	left	pane	to	explore
the	content	of	the	case	study	before	you	answer	the	questions.	Clicking	these	buttons	displays	information	such
as	business	requirements,	existing	environment	and	problem	statements.	If	the	case	study	has	an
All	Information	tab,	note	that	the	information	displayed	is	identical	to	the	information	displayed	on	the	subsequent
tabs.	When	you	are	ready	to	answer	a	question,	click	the	Question	button	to	return	to	the	question.
Overview	-
Contoso,	Ltd.	is	a	manufacturing	company	that	produces	sports	equipment.	Contoso	holds	quarterly	board
meetings	for	which	financial	analysts	manually	prepare
Microsoft	Excel	reports,	including	balance	sheets	and	profit	and	loss	statements	for	each	of	the	company's	four
business	units.
Existing	Environment	-
Data	and	Sources	-
Data	for	the	reports	comes	from	the	sources	shown	in	the	following	table.
The	balance	sheet	data	is	unrelated	to	the	profit	and	loss	results	other	than	they	both	relate	to	dates.
Balance	Sheet	Data	-

**Réponse exacte :**
C

**Explication courte :**
C	is	the	answer.	The	database	is	on	Azure	database,	not	on-premise
"Scheduled	refresh	of	reports	isn’t	supported	with	Dynamics	365	(on-premises)	datasets	that	are	published	to
the	Power	BI	service.	You	can	refresh	reports	using	in	Microsoft	Power	BI	Desktop	or	Microsoft	Office	Excel
and	then	upload	the	reports	to	the	Power	BI	service."
So	D	is	impossible.	C	is	correct.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the

---

## Question 301
**Énoncé de la question :**
C	is	the	answer.	The	database	is	on	Azure	database,	not	on-premise
"Scheduled	refresh	of	reports	isn’t	supported	with	Dynamics	365	(on-premises)	datasets	that	are	published	to
the	Power	BI	service.	You	can	refresh	reports	using	in	Microsoft	Power	BI	Desktop	or	Microsoft	Office	Excel
and	then	upload	the	reports	to	the	Power	BI	service."
So	D	is	impossible.	C	is	correct.
Introductory	Info
	Case	Study	-
This	is	a	case	study.	Case	studies	are	not	timed	separately.	You	can	use	as	much	exam	time	as	you	would	like	to
complete	each	case.	However,	there	may	be	additional	case	studies	and	sections	on	this	exam.	You	must	manage
your	time	to	ensure	that	you	are	able	to	complete	all	questions	included	on	this	exam	in	the	time	provided.
To	answer	the	questions	included	in	a	case	study,	you	will	need	to	reference	information	that	is	provided	in	the

**Réponse exacte :**
B

**Explication courte :**
Note:
Analysts	must	be	able	to	create	new	reports	from	the	dataset	that	contains	the	profit	and	loss	data,	but	the
reports	built	by	the	analysts	must	NOT	be	included	in	the	quarterly	reports	for	the	board.
Analysts	must	NOT	be	able	to	make	new	reports	by	using	the	balance	sheet	data.
Two	datasets	are	required.
Need	DAX	for:	A	comparison	of	quarterly	revenue	versus	the	same	quarter	from	the	previous	year.	Also	see
other	questions	in	this	Case	study	which	uses	DAX	expressions.
Incorrect:
Not	Direct	Query:	Direct	Query	Limited	Transformations.
You	are	not	able	to	use	all	of	the	normal	Power	Query	transformation	features.	Particular	DAX	functions	are
not	available	in	this	method	as	well.	So	if	your	data	is	poorly	structured	or	needing	lots	of	transformation,
sometimes	Direct	Query	is	not	a	viable	option.
Reference:
https://www.tessellationtech.io/import-vs-direct-query-power-bi/
	
	
Thank	you
Thank	you	for	being	so	interested	in	the	premium	exam	material.	
I'm	glad	to	hear	that	you	found	it	informative	and	helpful.
	
If	you	have	any	feedback	or	thoughts	on	the	bumps,	I	would	love	to	hear	them.	
Your	insights	can	help	me	improve	our	writing	and	better	understand	our	readers.
Best	of	Luck
You	have	worked	hard	to	get	to	this	point,	and	you	are	well-prepared	for	the	exam
Keep	your	head	up,	stay	positive,	and	go	show	that	exam	what	you're	made	of!
	
	
	
	
	
	
	
Total:	
301	Questions
Link:	
https://certyiq.com/papers/microsoft/pl-300
	
	Feedback	
More	Papers

---
