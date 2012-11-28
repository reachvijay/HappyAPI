*Happyfox API Technical Reference* [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)

#user

A User is a person opening a ticket on the Helpdesk.

###Operations

* [Read all users](#read-all-users)
* [Read one user by ID](#read-one-user-by-id)
* [Read one user by email](#read-one-user-by-email)

###Read All users
<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/users/?size=&lt;size&gt;&amp;page=&lt;page&gt;
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
				Paginated List of User
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
<p align="right"><a href="#operations">Top</a></p>
###Read One user By ID

Retrieve details of a user using their ID.

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/user/&lt;id&gt;/
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
				user
			</td>
		</tr>
	</table>


#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>
###Read One user By Email
Retrieve details of a user using the their email address.

<table><tr>
			<td>
				<b>URL</b>
			</td>
			<td>
				&lt;base_url&gt;/&lt;response_format&gt;/user/&lt;email&gt;/
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
				user
			</td>
		</tr>
	</table>

#####Data Structure
#####Code Example
<p align="right"><a href="#operations">Top</a></p>