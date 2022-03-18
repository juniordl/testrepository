Estas en una API Rest desarrollada en C# con .NET Core, realiza las llamadas de un ascensor a traves de los siguientes metodos

### Call

End point: http://localhost:6015/api/elevator/call
Body:
```json
{
    "Floor": 18,
    "CallType": 0
}
```

Floor: piso desde el cual se llama o al cual se quiere dirigir,
CallType: tipo de llamada donde 0 en desde dentro del ascensor y 1 es desde el exterior.

Puede realizar N llamadas de forma asincrona y puede visualizar la lista de los pisos por visitar en el siguiente metodo.

### Status

End Point: http://localhost:6015/api/elevator/status

No requiere de ningún parametro. Aquí se muestra el piso actual el cual irá incrementando de acuerdo al tiempo que se haya configurado en la aplicación (appconfig.json)
Ademas de la lista de llamadas al ascensor y el estado del mismo el cual indica si se encuentra esperando, de subida o de bajada
