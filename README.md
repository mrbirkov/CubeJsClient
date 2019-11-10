# CubeJsClient

[Cube.js](https://github.com/cube-js/cube.js) client for python!

```python
from CubeJsClient import CubeJsClient
my_client = CubeJsClient("http://my_cubejs_server.com/", "thesecret")
results = my_client.load({"measures": ["Cube.count"],"dimensions": ["Cube.dimension"]})
print(results)
```
