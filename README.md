
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

* [Tickets](https://github.com/reachvijay/HappyAPI/blob/master/sections/tickets.md)
* [Ticket Category](https://github.com/reachvijay/HappyAPI/blob/master/sections/category.md)
* [Ticket Status](https://github.com/reachvijay/HappyAPI/blob/master/sections/status.md)
* [Ticket Priority](https://github.com/reachvijay/HappyAPI/blob/master/sections/priority.md)
* [Custom Fields](https://github.com/reachvijay/HappyAPI/blob/master/sections/customfields.md)
* [Staff](https://github.com/reachvijay/HappyAPI/blob/master/sections/staff.md)
* [User](https://github.com/reachvijay/HappyAPI/blob/master/sections/user.md)
* [Protocols, Data Formats and Mechanisms](https://github.com/reachvijay/HappyAPI/blob/master/sections/protocols.md)



