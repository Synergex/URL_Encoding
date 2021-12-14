# URL_Encoding<br />
**Created Date:** 1/7/2003<br />
**Last Updated:** 10/19/2010<br />
**Description:** Function that returns a URL encoded string for use with the HTTP protocol. (Update for Synergy 9.5 compatibility)<br />
**Platforms:** Windows; Unix; OpenVMS<br />
**Products:** HTTP API<br />
**Minimum Version:** 8.1<br />
**Author:** Steve Ives
<hr>

**Additional Information:**
When passing data via the HTTP protocol, either as URI parameters in an HTTP GET
operation, or as body data in an HTTP POST operation, certain characters must be
'escaped', usually by replacing them with their hexadecimal values. This process
is referred to as "URL Encoding".

More details can be found in RFC 2396 (URI General Syntax)

This function accepts a string in parameter 1 and returns a URL encoded version
of that string.

This function must be declared before use, as follows:

external function
url_encode ,a

An example of using this function is:

url = "http://www.domain.com/page.asp?location=" + %url_encode("Gold River (CA)")

Which would set the variable url to:

http://www.domain.com/page.asp?location=Gold+River+%28CA%29
