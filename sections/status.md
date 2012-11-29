 <p align="right">*Happyfox API Technical Reference* | [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)</p>
#Tickets Status

A Ticket Category is a grouping of tickets based on a common attribute like ticket purpose, product or service, support type or department.

<div id="operations"></div>
###Operations

* [Read all statuses](#read-all-statuses)
* [Read one status](#read-one-status)

###Read All Statuses

<table width="90%"><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/statuses/
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
				Status
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One Status

<table width="90%"><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/status/&lt;id&gt;/
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
				Status
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example

<p align="right"><a href="#operations">Top</a></p>