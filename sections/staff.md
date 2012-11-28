*Happyfox API Technical Reference* [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)

#Staff

A Staff is a person handling Helpdesk duties like responding to incoming tickets, solving the requests / problems covered in the tickets.

###Operations

* [Read all staff](#read-all-staff)
* [Read one staff by ID](#read-one-staff-by-id)
* [Read one staff by email](#read-one-staff-by-email)

###Read All Staff
Retrieve a list of all staff

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_uri&gt;/&lt;response_format&gt;/staff/
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
				List of Staff
			</td>
		</tr>
	</table>


#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One Staff By ID

Retrieve details of a staff using their ID

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_uri&gt;/&lt;response_format&gt;/staff/&lt;id&gt;/
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
				Staff
			</td>
		</tr>
	</table>


#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One Staff By Email
Retrieve details of a staff using the their email address

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_uri&gt;/&lt;response_format&gt;/staff/&lt;email&gt;/
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
				Staff
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>