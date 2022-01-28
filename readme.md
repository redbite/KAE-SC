<h1>Keep an Eye on It: SALARY CHECKER</h1>
<p align="center">
<img src="https://i.imgur.com/xkLdpZI.png">
</p>
<section>Don't want to drain your salary as quick as you use to do?<br><b>Keep an Eye on It: Salary Checker</b> is a Java project developed to better manage your monthly expenses.<br>
<br>
<ul>
	<li>Classes</li>
	<li>Exceptions</li>
	<li>Output</li>
	<li>Main</li>
</ul>

<br>
<h2>CLASS</h2>
<ul>
	<li>Outcome<br>
	Each expense has an amount and a description.</li>
	<li>Salary<br>
	Each Salary has a single income, and several outcomes.<br>All the outcomes are stored in an HashMap with key: Integer (auto incrementing id) and a value (outcome).<br>It has these methods worth mentioning:
		<ul>
			<li><h4>printOutcomeHashMap</h4>Prints the outcomes stored in the Salary Hashmap.</li>
			<li><h4>setSingleOutcome</h4></li>
			<li><h4>incomeGraphics</h4>Used to better display the infos for Salary.</li>
			<li><h4>printSalary</h4></li>
		</ul>
	</li>
	<li>Year<br>
		<ul>
			<li><h4>Add/Remove Month</h4></li>
		<li><h4>getMonths</h4>Returns the HashMap<Integer,Salary> which represents the year's months.</li>
		<li><h4>compareTo</h4>Year implements Comparable<Year>, compareTo is used to set the year String as parameter to order the ArrayList in the main.</li>
		</ul>
	</li>
	<li>FileReaderAndWriter<br>
	It gives persistence to the program by loading all the already saved values and by storing the new ones into files that can be used as the project storage system.
	<br>It has 2 methods:
		<ul>
			<li><h4>writingFile</h4>
			Given a YEARS ArrayList, the method iterates through it and saves all its data in a txt file, created in order to save the data and making therefore possible for the readingFile method to load the already existing data.
			<br>Everytime it's called, it overwrites the txt file deleting the old content.</li>
			<li><h4>readingFile</h4>
			Given an already existing txt file written by the previous "writingHashMap" method, it saves the txt file data into the YEARS ArrayList.</li>
		</ul>
	</li>
	<li>Utils<br>
		This class has static methods and attributes used without any instance for this class by all the others Classes. 
		<ul>
			<li>ANSI_COLOR_CODES</li>
			<li><h4>MonthToInt</h4>Given a string, returns an integer from 0 to 11, or -1.</li>
			<li><h4>Intro</h4>KAE-SC logo, displayed on the boot-up.</li>
			<li><h4>Menu</h4>the main's possible choices.</li>
		</ul>
		It also has the <em>ANSI colour codes</em> used by either Salary and Salarycheck_main.
	</li>
</ul>

<h2>EXCEPTION</h2>
		WORK IN PROGRESS
<ul>
	<li>GenericException
	GenericException description<br>
	</li>
	<!-- <li></li> -->

</ul>
<h2>MAIN</h2>
<ul>
	<li>SalaryChecker_Test
	Has an <b>HashMap</b> for every year (12 months, <Integer> key (1 aka January, 2 February and so on...), <Salary> value))<br>
	Has a method (monthToInt) used to convert String month names to Integers (which returns -1 if the month name is not valid), and a menù method to show all the options.<br>
		The above methods are both static, as they are called inside the main.<br>
		<h3>MENU'</h3>
	<br>The menù contains several options:
				<p align="center">
					<img src="https://i.imgur.com/KorLUsN.png">
				</p>
		<ul>
			<li><b>Add Salary</b><br>
			Given a month name (e.g. November), through the MonthToInt method, the main allocates the Salary in its position in the HashMap(e.g. November = 11):
			<p align="center">
					<img src="https://i.imgur.com/jkdc7VL.png">
				</p>
			If the inserted month already exists (AKA: the place into the HashMap is already taken), it will be resetted with the new parameters.
			<br>In other words, if a month needs to be erased,  the add functionality can be used in order to reinitialize it.</li>
			<li>Remove Salary (WIP)<br>
				Given a month name (and a Year), its info are deleted (its expenses too).</li>
			<li>Add Expense<br>
			Given an amount, a description and a month, the expense is added (subtracted) to the Salary which has the same month.
			<p align="center">
					<img src="https://i.imgur.com/VQrM62u.png">
				</p></li>
			<li>Remove Expense <b>(WIP)</b><br>
				Given a month name (and a Year), followed by an ID (visible in the Print), the specific expense is deleted.</li>
			<li>Print all the months for the year:
			<p align="center">
					<img src="https://i.imgur.com/giF6Zvc.png">
				</p></li>
			<li>Menù<br>
			Prints all the possibilities</li>
			<li>Read from file<br>
				Read a txt file importing all the previously saved elements.
				<p align="center">
					<img src="https://i.imgur.com/luOYqAY.png">
				</p>
			</li>
			<li>Write file<br>
			Writes all the data in a txt file, in order to retrieve those through the readingFile method.
				<p align="center">
					<img src="https://i.imgur.com/B2S4jnF.png">
				</p>
			</li>
		</ul>
	</li>
</ul>
</section>
	
