# chatgpt-example-plugin
An example ChatGPT plugin based on the [documented example](https://platform.openai.com/docs/plugins/examples).

# Requirements
- [Python](https://www.python.org/downloads/)
- [Pip](https://pypi.org/project/pip/)
- [quart](https://pypi.org/project/quart/)
- [quart_cors](https://pypi.org/project/quart-cors/)

# Usage

Run the plugin:

```sh
$ python3 app.py
```

Create a TODO for a user:

```sh
$ curl -X POST http://localhost:5002/todos/<my_test_username> -H 'Content-Type: application/json' -d '{"todo": "vacum"}'
```

Get the TODOs for the user:

```sh
$ curl http://localhost:5002/todos/<my_test_username>
["vacum"]
```

Delete the TODO:

```sh
$ curl -X DELETE http://localhost:5002/todos/<my_test_username> -H 'Content-Type: application/json' -d '{"todo_idx": 0}'
```

Verify the TODO has been deleted:

```sh
$ curl http://localhost:5002/todos/<my_test_username>
[]
```
