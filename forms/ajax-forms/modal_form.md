Example for Manufacturer Model



**button that opens modal**
```

button.btn.btn-info data-target="#myModal" data-toggle="modal" type="button"  Adicionar Fabricante
```


**modal content**
```

  must have the same id of the data-target in button
#myModal.modal.fade role="dialog"
  .modal-dialog
    /! Modal content
    .modal-content
      .modal-header
        button.close data-dismiss="modal" type="button"  &times;
        h4.modal-title Adicionar Fabricante
      .modal-body
        = render 'manufacturers/form'
      .modal-footer
        button.btn.btn-default data-dismiss="modal" type="button"  Cancelar

```
