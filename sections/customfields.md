*Happyfox API Technical Reference* [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)

#Custom Fields

Custom fields allow additional data to be added to the Helpdesk as required. Custom fields can be defined for independently for users and tickets. For example, a phone number custom field can be added for users.

###Operations

* [Read all user custom fields](#read-all-user-custom-fields)
* [Read one user custom field](#read-one-user-custom-field)
* [Read all ticket custom fields](#read-all-ticket-custom-fields)
* [Read one ticket custom field](#read-one-ticket-custom-field)

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
