# Resmo Custom Data Resource/Schema Examples
## Example data:
```
{
  "employeeId": "18129",
  "employee": {
      "name": "lorem ipsum",
      "username": "lipsum",
      "email": "info@resmo.com"
  },
  "createdAt": "2016-11-24",
  "department": "Integrations",
  "salary": 1230.0,
  "manager": "test",
  "active": true
}
```
## Schema for example data:
```
{
	"type": "object",
	"resmo": {
		"id": "employeeId",
		"name": "$.employee.username",
		"importantFields": [
			"employeeId",
			"employee",
			"active"
		]
	},
	"title": "Employee Schema",
	"$schema": "https://json-schema.org/draft/2020-12/schema",
	"properties": {
		"active": {
			"type": "boolean",
			"default": false
		},
		"salary": {
			"type": "number",
			"default": 0
		},
		"manager": {
			"type": "string",
			"default": ""
		},
		"employee": {
			"type": "object",
			"properties": {
				"name": {
					"type": "string",
					"default": ""
				},
				"email": {
					"type": "string",
					"default": ""
				},
				"username": {
					"type": "string",
					"default": ""
				}
			}
		},
		"createdAt": {
			"type": "string",
			"default": ""
		},
		"department": {
			"type": "string",
			"default": ""
		},
		"employeeId": {
			"type": "string",
			"title": "The employeeId Schema",
			"examples": [
				"18129"
			]
		}
	}
}
```
