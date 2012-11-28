*Happyfox API Technical Reference* [Home](../happyfox_main.md)


#Tickets

###Operations Allowed On a Ticket

* [Read all tickets](tickets.md#read-all-tickets)
* [Read one ticket](tickets.md#read-one-ticket)
* [Create a ticket](tickets.md#create-a-ticket)
* [Add a staff update](tickets.md#add-a-staff-update)
* [Add a staff private note](tickets.md#add-a-staff-private-note)
* [Add a user reply](tickets.md#add-a-user-reply)


###Read All Tickets

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/tickets/?size=&lt;size&gt;&amp;page=&lt;page&gt;
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
				Paginated List of Ticket
			</td>
		</tr>
		<tr>
			<td rowspan="2">
				<b>Additional Params</b>
			</td>
			<td>
				size: number of items per page 	
				(minimum 10, maximum 50, default 10)
			</td>
		</tr>
		<tr>
			<td>
				page: the number of the page required
			</td>
		</tr>
</table>
#####Data Structure


#####Code Example

###Read One Ticket

<table><tbody><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket/&lt;id&gt;/
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
			</td>
		</tr>
	</tbody>
</table>	

#####Data Structure
#####Code Example
###Create a Ticket

To create a ticket make a POST request to the URL below with request data encoded in one of the supported formats. On success it returns the newly created ticket.*NOTE: file attachments are supported only when using Multipart Form Data*
<table><tbody><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/tickets/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				POST
			</td>
		</tr>
		<tr>
			<td>
				<b>Request Data</b>
			</td>
			<td>
				Create Ticket or Create Ticket Using User Email &amp; Name
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				Ticket
			</td>
		</tr>
	</tbody>
	</table>

###Add a Staff Update
To add a staff update make a POST request to the URL below with request data encoded in one of the supported formats. On success it returns the modified ticket.
*NOTE: file attachments are supported only when using Multipart Form Data*
<table><tbody><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket/&lt;id&gt;/staff_update/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				POST
			</td>
		</tr>
		<tr>
			<td>
				<b>Request Data</b>
			</td>
			<td>
				Add
				Staff Update
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				Ticket
			</td>
		</tr>
	</tbody>
</table>
#####Data Structure
#####Code Example

###Add a Staff Private Note
To add a staff private note make a POST request to the URL below with request data encoded in one of the supported formats. On success it returns the modified ticket.
<table><tbody><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket/&lt;id&gt;/staff_pvtnote/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				POST
			</td>
		</tr>
		<tr>
			<td>
				<b>Request Data</b>
			</td>
			<td>
				Add
				Staff Private Note
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				Ticket
			</td>
		</tr>
	</tbody>
	</table>
###Add a User Reply

To add a user reply make a POST request to the URL below with request data encoded in one of the supported formats. On success it returns the modified ticket.
*NOTE: file attachments are supported only when using Multipart Form Data*
<table><tbody><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/ticket/&lt;id&gt;/user_reply/
			</td>
		</tr>
		<tr>
			<td>
				<b>HTTP Method</b>
			</td>
			<td>
				POST
			</td>
		</tr>
		<tr>
			<td>
				<b>Request Data</b>
			</td>
			<td>
				Add
				User Reply
			</td>
		</tr>
		<tr>
			<td>
				<b>Response Data</b>
			</td>
			<td>
				Ticket
			</td>
		</tr>
	</tbody>
	</table>

