<link rel="stylesheet" href="https://github.com/reachvijay/HappyAPI/blob/master/css/style.css"></link>
<div id="headersec">

</div>
<div id="menu"></div>
#HappyFox API Technical Reference

The API provided by the Helpdesk is a RESTful web service. It supports operations like creating a ticket, adding updates to a ticket, listing tickets and users of the Helpdesk, etc. It supports JSON, YAML, XML, Form Urlencoded and Multipart Form Data formats.

##Requirements

The API requires following skills in any programming language.

1. Making HTTP requests (using GET and POST HTTP methods as a minimum requirement).

2. Doing HTTPBasicAuthentication.

3. Generatingandreadingdatainanyoneoftheformats-JSON,YAMLorXML.

4. Optionally making HTTP POST requests using content type of "multipart/form-data" (needed for ticket attachments)

##Documentation Conventions

The documentation indicates parameters that need to be replaced with actual values using the format <parameter_name>. The entire string including the enclosing < and > should be replaced.


*For example: if the parameter is <email> it should be replaced with the required email address*

##Topics

* [Tickets](sections/tickets.md)
* [Ticket Category](sections/category.md)
* [Ticket Status](sections/status.md)
* [Ticket Priority](sections/priority.md)
* [Staff](sections/staff.md)
* [Priority](sections/priority.md)
* [Protocols, Data Formats and Mechanisms](sections/protocols.md)



