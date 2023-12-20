# QUESTION: Get Employees by Department (Arrays Practice)

You are working on a Node.js application that manages a list of employees in a company.
The employee data is represented as an `array of arrays`, where each inner array contains information about an employee.
The inner array follows the format `[name, position, department]`.

Your task is to implement a `function` that retrieves all the employees in a specific department from the employee data array.
Write a function called `getEmployeesByDepartment` that takes `two parameters`: `employees` (the array of employee data) and `department` (the department name).
The function should return an `array of employees` who belong to the specified department.

Here are the requirements for the function:

- The employees array contains `multiple inner arrays`, where each inner array represents an employee and contains three elements: name, position, and department.
  For example: ['John Doe', 'Software Engineer', 'Engineering'].
- The function should search through the employees array and extract all the employees who belong to the specified department.
- The function should return an `array of employee names` who belong to the specified department.
- If there are no employees in the specified department, the function should return an `empty array.`
- The function should not modify the original employees array.
- Your task is to implement the getEmployeesByDepartment function according to the requirements.
- Use a callback for your solution

Here is an example data-set:

```js
const employees = [
	// Name         Position             Department
	['John Doe', 'Software Engineer', 'Engineering'],
	['Jane Smith', 'Product Manager', 'Product'],
	['Mike Johnson', 'Sales Executive', 'Sales'],
	['Emily Brown', 'HR Coordinator', 'Human Resources'],
	['David Lee', 'Quality Assurance', 'Engineering'],
	//  0              1                  2
];
```

Please provide your solution below.

```js
/**
 * Retrieve list of employee names from specified department
 *
 * @param {Array<Array>} employees Array of employees
 * @param {String} department Name of the target department
 * @return {Arra<String>} Array of employee names
 *
 */
function getEmployeesByDepartment(employees, department) {
	const employeeNames = [];

	// Processing
	// - loop through the employees
	employees.forEach(function (employee) {
		// - if department value = employee[2] value (the employee department)
		const employeeDepartment = employee[2];
		if (department === employeeDepartment) {
			// - push employee name (employee[0]) into the employeeNames array
			const employeeName = employee[0];
			employeeNames.push(employeeName);
		}
	});

	return employeeNames;
}

console.log(
	"getEmployeesByDepartment(employees, 'Engineering')",
	getEmployeesByDepartment(employees, 'Engineering')
);
```
