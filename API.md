## Base URL

`http://requestb.in/api/v1`

## Cross Domain Browser Requests

On newer browsers, you can just use XHR on the API directly since we support CORS. Alternatively, you can use JSONP by adding `?jsonp=yourCallback` to the request URI from a `<script>` tag.  

## Reference

### `POST /bins`

Create a new bin and return a JSON representation. 

Example response:

`{"color": [100, 70, 240], "name": "1as7yx51", "private": false, "request_count": 1}`

### `GET /bins/:bin_name`

Get a bin by name and return a JSON representation. 

Example response:

`{"color": [100, 70, 240], "name": "1as7yx51", "private": false, "request_count": 1}`

### `GET /bins/:bin_name/requests`

Get all the requests for a bin and return a JSON representation. 

Example response:

`[{"content_length": 15, "body": "", "form_data": [["foo", "bar"], ["bar", "foo"]], "remote_addr": "127.0.0.1", "method": "POST", "headers": {"Content-Length": "15", "Content-Type": "application/x-www-form-urlencoded", "Host": "localhost:5000", "Accept": "*/*", "User-Agent": "curl/7.21.4 (universal-apple-darwin11.0) libcurl/7.21.4 OpenSSL/0.9.8r zlib/1.2.5"}, "content_type": "application/x-www-form-urlencoded", "time": 1352503956.021339, "query_string": "", "path": "/1as7yx51", "id": "n535p0"}]`

### `GET /bins/:bin_name/requests/:request_name`

Get a single request by name for a bin and return a JSON representation. 

Example response:

`{"content_length": 15, "body": "", "form_data": [["foo", "bar"], ["bar", "foo"]], "remote_addr": "127.0.0.1", "method": "POST", "headers": {"Content-Length": "15", "Content-Type": "application/x-www-form-urlencoded", "Host": "localhost:5000", "Accept": "*/*", "User-Agent": "curl/7.21.4 (universal-apple-darwin11.0) libcurl/7.21.4 OpenSSL/0.9.8r zlib/1.2.5"}, "content_type": "application/x-www-form-urlencoded", "time": 1352503956.021339, "query_string": "", "path": "/1as7yx51", "id": "n535p0"}`
