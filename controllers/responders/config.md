**Console**

```
rails g responders:install
```

**ApplicationController/Custom global controller**

```ruby
self.responder = ApplicationResponder
respond_to :html
```

**responders.pt-br.yml**

```ruby
pt-BR:
  flash:
    actions:
      create:
        notice: "%{resource_name} criado com sucesso."
        alert: '%{resource_name} could not be created.'
      update:
        notice: "%{resource_name} atualizado com sucesso."
      destroy:
        notice: "%{resource_name} apagado com sucesso."
        alert: "%{resource_name} erro ao deletar."
```
