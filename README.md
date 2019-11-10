# CubeJsClient

[Cube.js](https://github.com/cube-js/cube.js) client for python!

## Docs

### CubeJsClient

#### init
```python
client = CubeJsClient(
    endpoint, # required - the running cube.js server
    secret, # required - the api token or secret needed for requests
    load_request_timeout=60, # optional - timeout for a single request to cube.js server
    load_waiting_max_requests=50, # optional - number of requests to make while waiting for a response
    load_waiting_interval=1, # optional - time to wait between requests
    token_ttl={'days': 1}, # optional - timedelta kwargs for how long the token is valid
    add_headers=None, # optional - any additional headers to add to the request
)
```

#### load
```python
client.load(
    request_body # required - json request to send to cube.js
)
```

## Example
```python
from CubeJsClient import CubeJsClient

my_client = CubeJsClient("http://my_cubejs_server.com/", "theApiToken", add_headers={'user_id': 1})
results = my_client.load({"measures": ["Cube.count"],"dimensions": ["Cube.dimension"]})

print(results)
```

## Future Work
- Requests for `sql` and for `meta`
- Comprehensive Documentation

## License

Cube.js Client is [MIT licensed](./packages/cubejs-client-core/LICENSE).