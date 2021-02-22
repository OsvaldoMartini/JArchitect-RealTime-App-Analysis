## ShiftHunter  - JMeter Performance Reports
* Before run this line
	* Delete the file previous File **"ShiftHunter_Performance_Test.csv"**
	* Delete the previous folder **"JMeter-Reports-ShiftHunter"**
```
	jmeter -n -t D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Tests_RestController.jmx -l D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Performance_Test.csv -e -o D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/JMeter-Reports-ShiftHunter/
	or
	ShiftHunter_Pattern_Tests_RestController
	jmeter -n -t D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Pattern_Tests_RestController.jmx -l D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Pattern_Performance_Test.csv -e -o D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/JMeter-Pattern-Reports-ShiftHunter/
	or for "C:/"
	jmeter -n -t C:/Martini/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Pattern_Tests_RestController.jmx -l C:/Martini/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Pattern_Performance_Test.csv -e -o C:/Martini/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/JMeter-Pattern-Reports-ShiftHunter/

```


### Report Summary
> Open the **index.html** whitin the Folder: 
```
		{Your Main Folder}/ShiftHunter_RealTime_RestController/Jmeter_Performance/JMeter-Reports-ShiftHunter/index.html
```

### Sequential Report Summary
```
	jmeter -n -t D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Tests_RestController.jmx -l D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Performance_Test-1.csv -e -o D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/HTMLReports-1/
	jmeter -n -t D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Tests_RestController.jmx -l D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Performance_Test-2.csv -e -o D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/HTMLReports-2/
	jmeter -n -t D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Tests_RestController.jmx -l D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/ShiftHunter_Performance_Test-3.csv -e -o D:/Projects/ShiftHunter_RealTime_RestController/Jmeter_Performance/HTMLReports-3/
```

### To run these agregations you will need to install JMeter Plugins
* **CMDRunner.jar** and  **JMeterPluginsCMD.jar**
	* Aggregate Report
```
	java -jar CMDRunner.jar  --tool Reporter --generate-csv Aggregate-ShiftHunter-50-Threads.csv --input-jtl out/test-results.csv --plugin-type AggregateReport
	java -jar JMeterPluginsCMD.jar --generate-csv Aggregate-ShiftHunter-50-Threads.csv --input-jtl testResults.jtl --plugin-type AggregateReport
```