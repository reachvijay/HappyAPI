 <p align="right">*Happyfox API Technical Reference* | [Home](https://github.com/reachvijay/HappyAPI/blob/master/README.md)</p>

#Protocols

This section of the document describes the communication protocol, data formats and application mechanisms used in the API.

###Sections


* [Request Methods](#request-methods)
* [Request Content Types](#request-content-types)
* [Response Content Types](#response-content-types)
* [Data Types](#data-types)
* [NULL Values](#null-values)
* [Paginated Lists for Collection Resources](#paginated-lists-for-collection-resources)
* [Data Validation Errors](#data-validation-errors)


###Request Methods

The following HTTP methods are used to perform operations on resources provided by the API.

*NOTE: not all resources support all the listed operations, see the documentation of each resource for the supported methods*

<table width="90%">
<tr>
			<td>
				<b>HTTP
				Method</b>
			</td>
			<td>
				<b>Operation</b>
			</td>
		</tr>
		<tr>
			<td>
				GET
			</td>
			<td>
				Retrieve a element or list of
				elements
			</td>
		</tr>
		<tr>
			<td>
				POST
			</td>
			<td>
				Create a new element or a child
				entry in a element
			</td>
		</tr>
		<tr>
			<td>
				PUT
			</td>
			<td>
				Update a element
			</td>
		</tr>
		<tr>
			<td>
				DELETE
			</td>
			<td>
				Delete a element
			</td>
		</tr>
</table>
<p align="right"><a href="#sections">Top</a></p>
###Request Content Types

The following data formats are supported by the API server when data is sent to it for POST and PUT operations.

Any of the data formats can be used provided the correct Content-Type is set in the HTTP request header.


*NOTE: file uploads are only supported with Multipart Form Data.*


<table width="90%"><tr>
		<td>
			<b>Request
			Format</b>
		</td>
		<td>
			<b>Content-Type</b>
		</td>
		<td>
			<b>File
			Upload</b>
		</td>
	</tr>
	<tr>
		<td>
			JSON
		</td>
		<td>
			application/json
		</td>
		<td>
			NO
		</td>
	</tr>
	<tr>
		<td>
			YAML
		</td>
		<td>
			application/x-yaml
		</td>
		<td>
			NO
		</td>
	</tr>
	<tr>
		<td>
			Form Urlencoded
		</td>
		<td>
			application/x-www-form-urlencoded
		</td>
		<td>
			NO
		</td>
	</tr>
	<tr>
		<td>
			Multipart Form Data
		</td>
		<td>
			multipart/form-data
		</td>
		<td>
			YES
		</td>
	</tr>
</table>

<p align="right"><a href="#sections">Top</a></p>
###Response Content Types

The following data formats are supported for response data sent back by the API server. The required data format is specified as the <response_format> mentioned under Resource URIs.

<table width="90%"><tr>
			<td>
				<b>Response
				Format</b>
			</td>
			<td>
				<b>Specified
				in URI as</b>
			</td>
			<td>
				<b>Response
				Content-Type</b>
			</td>
		</tr>
		<tr>
			<td>
				JSON
			</td>
			<td>
				json
			</td>
			<td>
				application/json
			</td>
		</tr>
		<tr>
			<td>
				YAML
			</td>
			<td>
				yaml
			</td>
			<td>
				application/x-yaml
			</td>
		</tr>
		<tr>
			<td>
				XML
			</td>
			<td>
				xml
			</td>
			<td>
				application/xml
			</td>
		</tr>
	</table>

<p align="right"><a href="#sections">Top</a></p>
###Data Types

These are the basic data types that are used in the API. Using these types more complex data structures for the resources are built.

<table width="90%"><tr>
			<td>
				<b>Type</b>
			</td>
			<td>
				<b>Description</b>
			</td>
		</tr>
		<tr>
			<td>
				String
			</td>
			<td>
				String type with Unicode support
			</td>
		</tr>
		<tr>
			<td>
				Integer
			</td>
			<td>
				Signed 64 bit integral number
			</td>
		</tr>
		<tr>
			<td>
				ID
			</td>
			<td>
				Special type of Integer with minimum value 1,
				Will be unique within each resource type
			</td>
		</tr>
		<tr>
			<td>
				Float
			</td>
			<td>
				Floating point number
			</td>
		</tr>
		<tr>
			<td>
				Boolean
			</td>
			<td>
				True/False type
			</td>
		</tr>
		<tr>
			<td>
				DateTime
			</td>
			<td>
				Combined date and
				time in the ISO 8601 extended format of YYYY-MM-DD
				HH:MM:SS.ssssss
				<br/>
				<i><b>NOTES</b>:<br/> 
				
				1. all DateTime values in the API are in UTC
				timezone<br/>
				2. the decimal part represented by ssssss is
				optional<br/>
				3. a space separator is used between the date
				and time values</i>
			</td>
		</tr>
		<tr>
			<td>
				Date
			</td>
			<td>
				<a name="firstHeading1"></a>Date in the ISO
				8601 extended format of YYYY-MM-DD<br/>
				<i><b>NOTE</b>: all Date values in the API are in</i>
				UTC timezone
			</td>
		</tr>
	</table>

<p align="right"><a href="#sections">Top</a></p>
###NULL Values

Some of the fields in a resource may be optional or currently absent . The values of these fields are represented as a special NULL value. This value maps to corresponding equivalents in the data formats as listed below.

<table width="90%"><tr>
			<td>
				<b>Response Format</b>
			</td>
			<td>
				<b>NULL Value Representation</b>
			</td>
		</tr>
		<tr>
			<td>
				JSON
			</td>
			<td>
				null
			</td>
		</tr>
		<tr>
			<td>
				YAML
			</td>
			<td>
				null
			</td>
		</tr>
		<tr>
			<td>
				XML
			</td>
			<td>
				Element attribute null="True"
			</td>
		</tr>
	</table>

<p align="right"><a href="#sections">Top</a></p>
###Paginated Lists for Collection Resources

Some of the collection resources provided by the API may return a large volume of elements. In these cases the API imposes a upper limit on the number elements that can be returned in a single collection read request.

By specifying a page size (lesser than or equal to the upper limit) and a corresponding page number as URL parameters, the collection can be split the into a smaller number of elements and progressively retrieved from the API server.


The response from the API server contains information about the page split and the actual data as described below.


#####URL Parameters

<table width="90%"><tr>
			<td>
				<b>Field</b>
			</td>
			<td>
				<b>Type</b>
			</td>
			<td>
				<b>Description</b>
			</td>
		</tr>
		<tr>
			<td>
				size
			</td>
			<td>
				Integer
			</td>
			<td>
				The number of items per page (limited to the
				maximum defined for the particular collection resource)
			</td>
		</tr>
		<tr>
			<td>
				page
			</td>
			<td>
				Integer
			</td>
			<td>
				The number of the page required
			</td>
		</tr>
	</table>

#####Paginated List - Response Data Structure

This data structure contains information and data from the paginated list.


<table width="90%"><tr>
			<td>
				<b>Field</b>
			</td>
			<td>
				<b>Type</b>
			</td>
			<td>
				<b>Description</b>
			</td>
		</tr>
		<tr>
			<td>
				page_info
			</td>
			<td>
				Page
				Info
			</td>
			<td>
				Information about the pagination
			</td>
		</tr>
		<tr>
			<td>
				data
			</td>
			<td>
				List of Elements
			</td>
			<td>
				The list of elements retrieved from the
				collection
			</td>
		</tr>
	</table>

#####Page Info - Inner Data Structure
This inner data structure is used in the "page_info" field of a Paginated List.

<table width="90%"><tr>
			<td>
				<b>Field</b>
			</td>
			<td>
				<b>Type</b>
			</td>
			<td>
				<b>Description</b>
			</td>
		</tr>
		<tr>
			<td>
				count
			</td>
			<td>
				Integer
			</td>
			<td>
				Number of elements returned
			</td>
		</tr>
		<tr>
			<td>
				start_index
			</td>
			<td>
				Integer
			</td>
			<td>
				The index of the first element in the returned
				subset
			</td>
		</tr>
		<tr>
			<td>
				end_index
			</td>
			<td>
				Integer
			</td>
			<td>
				The index of the last element in the returned
				subset
			</td>
		</tr>
		<tr>
			<td>
				last_index
			</td>
			<td>
				Integer
			</td>
			<td>
				The index of the last element in the entire
				collection
			</td>
		</tr>
		<tr>
			<td>
				page_count
			</td>
			<td>
				Integer
			</td>
			<td>
				Number of pages for the given page size
			</td>
		</tr>
	</table>

<p align="right"><a href="#sections">Top</a></p>
###Data Validation Errors

The API server performs validation on the data submitted via POST and PUT requests. In case the data validation fails, the API server returns HTTP response code 400 along with error information in the response body.

The error information response data is a List of Field Errors that contains information about data validation errors in individual fields as well as any errors that apply to the entire request (like errors that are not dependent on individual fields).

#####Field Errors - Response Data Structure

This data structure contains the field name and the list of errors messages for the field.


<table width="90%"><tr>
			<td>
				<b>Field</b>
			</td>
			<td>
				<b>Type</b>
			</td>
			<td>
				<b>Description</b>
			</td>
		</tr>
		<tr>
			<td>
				field
			</td>
			<td>
				String
			</td>
			<td>
				The name of the field.
				(For errors that pertain to the entire request
				and not to a particular field, the field name will be "__all__")
			</td>
		</tr>
		<tr>
			<td>
				errors
			</td>
			<td>
				List of String
			</td>
			<td>
				One or more errors related to the field value
			</td>
		</tr>
	</table>
	
<p align="right"><a href="#sections">Top</a></p>