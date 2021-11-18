# Advance Node.js Interview Question

## 1. Ways to secure Node.js code

 1. Validate user input to limit **SQL injections** and **XSS attacks**
	 ### SQL injections
	 Input values must be validated else the attacker can send and run queries using the input values.  e.g :
	 
	 ```
	 connection.query('SELECT * FROM orders WHERE id = ' + id, function (error, results, fields) {
	  if (error) throw error;
	  // ...
	  }); 
	  
Here the value id must be validated, instead of sending just `4564` (the id of the order), the attacker can send `4564; DROP TABLE ORDERS;`  and Node.js will wipe your entire table.

### XSS attacks

Cross-Site Scripting (XSS) attacks work similarly to SQL injections. The difference is that instead of sending malicious SQL, the attacker is able to execute JavaScript code.

Cross-Site Scripting (XSS) attacks work similarly to SQL injections. The difference is that instead of sending malicious SQL, the attacker is able to execute JavaScript code.

  
