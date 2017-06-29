### Create Employee and Contract at the same time

```ruby
#app/models/employee.rb

has_one :contract, inverse_of: :employee

accepts_nested_attributes_for :contract
```

```ruby
#app/models/contract.rb

belongs_to :employee
```

```ruby
#app/controllers/employees_controller.rb

def employee_params
    params.require(:employee).permit(:name,:email,:telephone,:cellphone,:zipcode,:number,:street,
      contract_attributes: [:id,:start_date,:end_date,:start_time,:end_time,:employee_id])
  end
```

```ruby-slim

  = form_for @employee do |f|

    = f.fields_for :contract, @employee.build_contract do |c|

      = c.text_field :start_date

```
