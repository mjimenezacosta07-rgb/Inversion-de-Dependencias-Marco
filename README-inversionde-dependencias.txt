Principio de Inversion de Dependencias
Las clases no deben depender de clases concretas, sino de abstracciones (son las interfaces)

o sea, una clase no debe de decir " necesito exactamente eel correo" sino que "nesecito alo que sepa recibir un correo" asi le puede sar a cualquiera cosa que cumpla con esto 

ejemplo: un cel no ocupa tener un cargador en especifico solo coupa el puerto correcto ósea le sirven varios cargadores 
Como se implementa en este código:::

1. Se crea la interfaz EnvioRecibo con el metodo virtual puro EnviarRecibo(). Esta es la
 abstraccion.
2. Hay dos clases concretas que heredan de EnvioRecibo y escriben ese metodo cada una a
 su manera: EnviarEmail (por correo) y EnviarApp (por la aplicacion).
3. La clase AdmProducto hace la compra. Su metodo Compra() recibe un puntero a
 EnvioRecibo, no a EnviarEmail ni a EnviarApp: