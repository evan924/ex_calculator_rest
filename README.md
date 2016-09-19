# ex_calculator_rest
The  SOAP based calculator web services demo refactored as RESTful

This example takes the SOAP based calculator web services demo that is shipped in the Genero product as FGLDIR/demo/WebServices/calculator and has refeactored it to use RESTful techniques.

It consists of two programs, calculatorServer and calculatorClient.  Build and run the calculatorServer example, leave it running, and then run the calculatorClient example.   Communication is controlled via FGLAPPSERVER environment variable.  The Studio project sets it to 8091, but you are free to change it to a different port.

The API uses a simple GET and a URL of the form ...

http://_address_/calculator?operator=_value_&param1=_value_&param2=_value_

Valid values for the operator argument are add, minus, multiply, and divide.
Valid values for param1, and param2 are any integer

The result is an XML Document of the form ...
```xml
    <CALCULATOR>
         <INPUT operator="add" param1="1" param2="2"/>
         <OUTPUT result="3" remaind="0"/>
    </CALCULATOR>
```
... where INPUT node contains details of what was passed, and OUTPUT node contains the results.

(Note: This example was written before JSON was added to Genero.  Its on my TODO list to add JSON to this example)
