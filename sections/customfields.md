 <p align="right">*Happyfox API Technical Reference* | [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)</p>

#Custom Fields

Custom fields allow additional data to be added to the Helpdesk as required. Custom fields can be defined for independently for users and tickets. For example, a phone number custom field can be added for users.

###Operations

* [Read all user custom fields](#read-all-user-custom-fields)
* [Read one user custom field](#read-one-user-custom-field)
* [Read all ticket custom fields](#read-all-ticket-custom-fields)
* [Read one ticket custom field](#read-one-ticket-custom-field)
* [Notes](#notes)

###Read All User Custom Fields

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/user_custom_fields/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				GET
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				List of User
				Custom Field
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One User Custom Field

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/user_custom_field/&lt;id&gt;/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				GET
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				User
				Custom Field
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example

<p align="right"><a href="#operations">Top</a></p>
###Read All Ticket Custom Fields

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket_custom_fields/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				GET
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				List of Ticket
				Custom Field
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One Ticket Custom Field

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket_custom_field/&lt;id&gt;/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				GET
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				Ticket
				Custom Field
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>

###Notes

#####Common Information For Setting Ticket / User Custom Field Values

1. When the "depends_on_choice" field of a custom field set to a non-NULL value, it is applicable only when the corresponding choice is selected. The "dependant_fields" field of Choice Item can also be used to determine which custom fields are applicable when the choice is selected.
2. Values for "multiple_choice" type custom fields should be sent as multiple fields with the same field name when using Form Urlencoded and Multipart Form Data formats. The values can be sent as List for JSON and YAML formats.

#####Ticket Custom Field Values For Create Ticket

1. All the points in Common Information For Setting Ticket / User Custom Field Values
2. The values for ticket custom fields should be appended to the fields for Create Ticket
3. The value for a ticket custom field should be sent using a field name constructed from the ID of the ticket custom field in the following format "t-cf-&lt;id&gt;"
4. The ticket custom fields applicable to a ticket are dependent on the ticket's category. This can be determined from the "categories" field of Ticket Custom Field

#####User Custom Field Values For Create Ticket

1. All the points in Common Information For Setting Ticket / User Custom Field Values
2. The values for user custom fields should be appended to the fields for Create Ticket
3. The value for a user custom fields should be sent using a field name constructed from the ID of the user custom field in the following format "c-cf-&lt;id&gt;"

<p align="right"><a href="#operations">Top</a></p>