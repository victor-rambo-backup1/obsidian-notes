
> Método que retorna valor de uma variável privada de uma classe

```python
class User:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name
```

### Observações
- O decorador `@propery` é necessário para declarar um método como getter