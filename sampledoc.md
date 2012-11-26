##Ticket Category - Resource
A Ticket Category is a grouping of tickets based on a common attribute like ticket purpose, product or service, support type or department.
### Operations
<table>
<tr><th></th><th>Reading All Categories</th><th>Reading One Category</th></tr>
<tr><td>URL</td><td>[base_uri]/[response_format]/categories/</td><td>[base_uri]/[response_format]/categories/[id]</td></tr>
<tr><td>HTTP Method</td><td>GET</td><td>GET</td></tr>
<tr><td>Response Data</td><td colspan="2">List of ticket category</td></tr>
</table>
###Data Structures
#####Ticket Category - Response Data StructureThis data structure contains information about a ticket category￼
<table>
<tr><th>Field</th><th>Type</th><th>Description</th></tr>
<tr><td>id</td><td>ID</td><td>Unique numerical identifier</td></tr>
<tr><td>name</td><td>String</td><td>Name of the category</td></tr>
<tr><td>description</td>String<td></td><td>Short description about the category</td></tr>
<tr><td>public</td><td>Boolean</td><td>If True, visible to users, else only visible to staff</td></tr>
</table>