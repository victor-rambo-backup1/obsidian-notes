
>Método que altera variável privada de uma classe, geralmente faz alguma checagem

```python
@property
def name(self):
    return self._name

@name.setter
def name(self, value):
    self._name = value
```

### Observações
- O decorador `@propery` é necessário para declarar um método como getter
- O decorador `@<nome-do-getter>.setter` é necessário para declarar um método como setter
- Podemos botar `raise` dentro do setter para levantar erros em casos de argumento inválido

