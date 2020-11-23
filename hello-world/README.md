# Hello World Plugin

## Methods

### `getHelloWorld`

Args : None<br>
Returns: `Hello World`<br>
Sample Config:
```yaml
- name: Hello World
  jarfile: helloworld.jar
  method: com.bbloggsbott.helloworld.HelloWorld.getHelloWorld
  endpoint: /helloworld
  requestType: GET
```

### `getHelloName`
Args :

| Arg Name | Arg Type |
|-|-|
|`name` | `java.lang.String` |

Returns: `Hello {{name}}`<br>
Sample Config:
```yaml
- name: Hello Name
  jarfile: helloworld.jar
  method: com.bbloggsbott.helloworld.HelloWorld.getHelloName
  endpoint: /hello
  requestType: GET
  args:
    - name: name
      type: java.lang.String
      requestParam: true
```

### `getHelloSum`
Args :

| Arg Name | Arg Type |
|-|-|
|`a` | `int` |
|`b` | `int` |

Returns: `{{a+b}}`<br>
Sample Config:
```yaml
- name: Sum
  jarfile: helloworld.jar
  method: com.bbloggsbott.helloworld.HelloWorld.getSum
  endpoint: /sum
  requestType: GET
  args:
    - name: a
      type: int
      requestParam: true
    - name: b
      type: int
      requestParam: true
    
```
