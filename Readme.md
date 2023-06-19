# Fundamentos de .Net

## Introducción a .NET:

### Qué es .NET y su propósito:
- .NET es un framework de desarrollo de software desarrollado por Microsoft. Proporciona un entorno para construir y ejecutar diferentes tipos de aplicaciones en múltiples plataformas.
- El propósito principal de .NET es permitir a los desarrolladores crear aplicaciones de alta calidad de forma rápida y eficiente, utilizando un conjunto de herramientas y librerías predefinidas.

### Diferencia entre .NET Framework, .NET Core y .NET:

**.NET Framework:** Es la versión original de .NET, diseñada para aplicaciones de Windows. Ofrece una amplia compatibilidad con bibliotecas y APIs de Windows, pero está limitada a la plataforma Windows.

**.NET Core:** Es una versión modular y multiplataforma de .NET. Permite desarrollar aplicaciones que se ejecutan en Windows, Linux y macOS. Proporciona una mayor flexibilidad y rendimiento que .NET Framework.

**.NET:** Es la última versión de .NET y combina las características de .NET Framework y .NET Core. Es una plataforma unificada y de código abierto que se puede utilizar para desarrollar aplicaciones en diferentes sistemas operativos.

### Ventajas y usos de .NET:

**Lenguajes de programación:** .NET admite varios lenguajes de programación, como C#, Visual Basic .NET, F#, entre otros, lo que brinda flexibilidad a los desarrolladores para elegir el lenguaje que mejor se adapte a sus necesidades.

**Portabilidad:** Con .NET Core y .NET 5, es posible crear aplicaciones que se ejecutan en múltiples plataformas, lo que permite llegar a más usuarios y dispositivos.

**Rendimiento:** .NET está diseñado para ofrecer un rendimiento eficiente y escalable. Proporciona características como la compilación en tiempo de ejecución y la gestión de memoria automática que ayudan a optimizar el rendimiento de las aplicaciones.

**Seguridad:** .NET incluye mecanismos de seguridad integrados, como la gestión de identidad y acceso, que facilitan la implementación de prácticas de seguridad en las aplicaciones.

**Amplia comunidad y soporte:** .NET cuenta con una gran comunidad de desarrolladores y un sólido soporte de Microsoft. Esto significa que hay abundante documentación, tutoriales y recursos disponibles para ayudar a los desarrolladores a aprender y resolver problemas en sus proyectos.

Es importante destacar que .NET es una tecnología en constante evolución y se recomienda estar al tanto de las últimas actualizaciones y versiones para aprovechar al máximo sus capacidades y beneficios.

## Instalación y configuración del entorno de desarrollo:

### Descarga e instalación del SDK de .NET:

Para comenzar a desarrollar en .NET, es necesario descargar e instalar el SDK (Software Development Kit) de .NET en tu máquina. El SDK incluye todas las herramientas necesarias para desarrollar, compilar y ejecutar aplicaciones en .NET.

Puedes descargar el SDK de .NET desde el sitio oficial de Microsoft. Visita la página de descargas de .NET (https://dotnet.microsoft.com/download) y selecciona la versión del SDK que desees utilizar (por ejemplo, .NET 5 o una versión posterior).

Sigue las instrucciones de instalación proporcionadas por el instalador del SDK para completar el proceso de instalación en tu sistema.

#### Instalación de Visual Studio o elección de otro IDE:

1. Visual Studio es el IDE (Integrated Development Environment) más popular para el desarrollo en .NET. Proporciona una amplia gama de herramientas y características para facilitar el desarrollo de aplicaciones en .NET.

2. Puedes descargar e instalar Visual Studio desde el sitio oficial de Microsoft (https://visualstudio.microsoft.com). Hay diferentes versiones disponibles, como Visual Studio Community (gratuita) y Visual Studio Professional (con funciones adicionales).

3. Sin embargo, si prefieres utilizar otro IDE, también hay opciones disponibles, como Visual Studio Code (un editor de código ligero y gratuito), JetBrains Rider, entre otros. Puedes elegir el IDE que mejor se adapte a tus necesidades y preferencias.

#### Configuración del entorno de desarrollo:

Una vez que hayas instalado el SDK de .NET y el IDE, es importante realizar algunas configuraciones iniciales en tu entorno de desarrollo.

Si estás utilizando Visual Studio, asegúrate de seleccionar la configuración adecuada para el desarrollo en .NET durante el proceso de instalación. Esto incluye la selección de los componentes y paquetes necesarios para el desarrollo en .NET.

También es recomendable actualizar Visual Studio y el SDK de .NET a las versiones más recientes para aprovechar las mejoras y correcciones de errores más recientes.

Además, puedes configurar las preferencias del IDE, como el tema, el estilo de codificación, las extensiones y otras opciones personalizadas según tus preferencias.

Es importante tener en cuenta que los pasos de instalación y configuración pueden variar dependiendo del sistema operativo y las versiones específicas de .NET y del IDE que estés utilizando. Siempre es recomendable consultar la documentación oficial y los recursos adicionales proporcionados por Microsoft para obtener instrucciones detalladas y actualizadas sobre la instalación y configuración del entorno de desarrollo.

## Estructura de un proyecto en .NET:

Antes de iniciar con la estructura de un proyecto en .Net, es necesario que puedas conocer los comandos principales que existen en .Net para trabajar.

- Para ver la lista de templates de proyectos
```{bash}
dotnet new --list
```
- Para crear un proyecto
```{bash}
dotnet new <tipo-proyecto>
```
- Para hacer correr nuestro proyecto
```{bash}
dotnet run
```
- Compila un proyecto y todas sus dependencias, tambien verificar que toda la sintaxis este bien y no se tengan problemas con dependencias
```{bash}
dotnet build
```
- Sirve restaurar las dependencias y las herramientas de un proyecto.
```{bash}
dotnet restore
```
- Nos permite ejecutar el proyecto y va revisando los cambios del proyecto en tiempo real (similar a nodemon en node)
```{bash}
dotnet watch run
```

- Nos permite conocer la versión del SDK que se está trabajando

```{bash}
dotnet --version
```
### Creación de un proyecto de consola en .NET:

Para empezar, vamos a crear un proyecto de consola en .NET utilizando el comando dotnet new en la línea de comandos. Abre una terminal o ventana de comandos y navega hasta la ubicación donde deseas crear tu proyecto.

Ejecuta el siguiente comando para crear un nuevo proyecto de consola en .NET:

```{bash}
dotnet new console -n MiProyecto
```
Esto creará un nuevo proyecto de consola llamado "MiProyecto" en una carpeta con el mismo nombre.

Después de ejecutar el comando, verás que se crearon varios archivos en la carpeta del proyecto, incluyendo un archivo Program.cs que contiene el código fuente principal de la aplicación de consola.

### Organización de carpetas y archivos:

La estructura de un proyecto en .NET puede variar según el tipo de proyecto y las preferencias del desarrollador. Sin embargo, en un proyecto de consola básico, la estructura típica de carpetas y archivos incluye lo siguiente:

**MiProyecto.csproj:** Este archivo es el archivo de proyecto principal en formato XML. Contiene la configuración y referencias del proyecto.

**Program.cs:** Este archivo contiene la clase principal Program que contiene el método Main, que es el punto de entrada de la aplicación. Aquí es donde se inicia la ejecución del programa.

### Archivos de compilación
ㅤ
Dentro del proceso de compilación tenemos dos carpetas relacionadas
ㅤ
📁 bin : Contiene el archivo compilado del proyecto .dll y más

📁 obj : Tiene los archivos que se generan en la compilación de manera temporal, par despues ser entregado al archivo bin.
ㅤ

💡 Para limpiar la compilación hecha, podemos usar el comando dotnet clean
ㅤ
Existen dos modos de compilación en .NET
ㅤ
##### modo debug

Prepara la aplicación para el uso en un ámbito de pruebas, suele ser un poco más pesado que el modo de compilado release. Se recomienda no usar este compilado en modo producción, ya que se puede exponer información que solo nos interesa que se muestre cuando estamos probando y no así cuando nuestros clientes lo ejecuten.
ㅤ
##### modo release

Prepara la aplicación para que esté lista en producción, tenga un mejor performance y rendimiento, además de que sea mucho más liviano. Elimina todos los archivos que no se necesitan en producción.

El comando que nos permite compilar a producción es
dotnet build --configuration release

Ideas/conceptos clavesㅤ

**.dll:** Es un archivo que viene una compilación de un lenguaje de alto nivel (ej. C#)
ㅤ
**.exe:** Es un archivo ejecutable que únicamente se utiliza en Windows, resumiendo su funcionamiento toma el archivo .dll y lo ejecuta en nuestro ordenador.

Además de estos archivos principales, también puedes tener otras carpetas y archivos dependiendo de las necesidades del proyecto, como carpetas para almacenar clases adicionales, recursos, configuraciones, pruebas, etc.

En la carpeta “bin” se encuentran los archivos compilados.
Comando para Eliminar archivos compilados
```{bash}
dotnet clean
```
2 modos de compilación en .NET

- Modo Debug

- Modo Release

```{bash}
dotnet build --configuration realease
```

Se crea la carpeta “Debug” y “Release”

Ahora es conveniente configurar el archivo global json con el siguiente comando.

```{bash}
dotnet new globaljson
```

### Compilación y ejecución de la aplicación:

Después de crear la estructura básica del proyecto, es hora de compilar y ejecutar la aplicación de consola.

Navega a la carpeta del proyecto en la línea de comandos y ejecuta el siguiente comando para compilar el proyecto:

```{bash}
dotnet build
```
Esto compilará el proyecto y generará el archivo ejecutable en la carpeta de salida predeterminada (por lo general, una carpeta llamada bin).

Una vez que se haya compilado exitosamente, puedes ejecutar la aplicación utilizando el siguiente comando:

```{bash}
dotnet run
```
Esto ejecutará la aplicación y mostrará la salida en la consola.

¡Felicidades! Has creado, compilado y ejecutado tu primer proyecto de consola en .NET.

Recuerda que estos pasos son solo una introducción básica a la estructura de un proyecto en .NET. A medida que avances en tu aprendizaje, podrás explorar y utilizar más funcionalidades y características avanzadas de .NET para desarrollar aplicaciones más complejas y personalizadas.

## Trabajo con clases y objetos:

### Creación de clases y definición de propiedades y métodos:

En .NET, las clases son la base de la programación orientada a objetos. Puedes crear tus propias clases para modelar entidades y definir sus propiedades y métodos.

Para crear una clase, puedes agregar un nuevo archivo .cs a tu proyecto y definir la estructura de la clase en ese archivo. Por ejemplo, crea un archivo llamado Persona.cs y agrega el siguiente código:

```{csharp}
public class Persona
{
    // Propiedades
    public string Nombre { get; set; }
    public int Edad { get; set; }
        
    // Métodos
    public void Saludar()
    {
        Console.WriteLine($"Hola, mi nombre es {Nombre} y tengo {Edad} años.");
    }
}
```
En este ejemplo, creamos una clase **Persona** con dos propiedades: **Nombre** y **Edad**, y un método **Saludar** que muestra un mensaje con el nombre y la edad de la persona.

### Encapsulamiento, herencia y polimorfismo:

El encapsulamiento es un principio de la programación orientada a objetos que permite ocultar y proteger los detalles internos de una clase. Puedes aplicar el encapsulamiento utilizando modificadores de acceso como public, private y protected para controlar el acceso a las propiedades y métodos de una clase.

La herencia es un concepto que te permite crear nuevas clases basadas en una clase existente. Puedes utilizar la palabra clave class seguida del nombre de la clase y : seguido del nombre de la clase base para heredar propiedades y métodos de la clase base.

El polimorfismo es la capacidad de una clase para tomar muchas formas. Puedes utilizar el polimorfismo para reemplazar o extender el comportamiento de los métodos heredados en clases derivadas.

### Instanciación de objetos y uso de constructores:

Para utilizar una clase, necesitas crear instancias u objetos de esa clase. Puedes hacerlo utilizando la palabra clave new seguida del nombre de la clase y paréntesis vacíos, o puedes utilizar constructores para proporcionar valores iniciales a las propiedades de la clase.

Por ejemplo, en tu programa principal Program.cs, puedes crear una instancia de la clase Persona y utilizar sus propiedades y métodos de la siguiente manera:

```{csharp}

static void Main()
{
    Persona persona = new Persona();
    persona.Nombre = "Juan";
    persona.Edad = 25;
    persona.Saludar();
}
```
En este ejemplo, creamos una instancia de la clase Persona llamada persona, establecemos los valores de las propiedades Nombre y Edad utilizando el operador de asignación (=) y luego llamamos al método Saludar() para mostrar el mensaje en la consola.

## Interacción con el usuario:

Utilización de la consola para solicitar y mostrar información al usuario:

En .NET, puedes utilizar la consola para interactuar con el usuario y solicitar o mostrar información.

Para solicitar información al usuario, puedes utilizar el método Console.ReadLine() que permite leer una línea de texto ingresada por el usuario. Por ejemplo:

```{csharp}
Console.WriteLine("Ingresa tu nombre:");
string nombre = Console.ReadLine();
```
En este ejemplo, se muestra un mensaje en la consola solicitando al usuario que ingrese su nombre, y luego se almacena la entrada del usuario en una variable llamada nombre.

Para mostrar información al usuario, puedes utilizar el método Console.WriteLine() que muestra una línea de texto en la consola. Por ejemplo:

```{csharp}

string mensaje = "¡Hola, bienvenido!";
Console.WriteLine(mensaje);
```
En este ejemplo, se muestra el mensaje "¡Hola, bienvenido!" en la consola.

### Validación de entrada de datos:

Es importante validar la entrada de datos del usuario para garantizar que cumpla con los requisitos esperados.

Puedes utilizar métodos como int.TryParse() o double.TryParse() para validar si la entrada del usuario es un número válido. Por ejemplo:

```{csharp}
Console.WriteLine("Ingresa tu edad:");
string entradaEdad = Console.ReadLine();

int edad;
if (int.TryParse(entradaEdad, out edad))
{
    Console.WriteLine($"Tu edad es: {edad}");
}
else
{
    Console.WriteLine("La entrada no es un número válido.");
}
```

En este ejemplo, se solicita al usuario que ingrese su edad y se utiliza int.TryParse() para intentar convertir la entrada a un número entero. Si la conversión es exitosa, se muestra la edad en la consola; de lo contrario, se muestra un mensaje de error.

### Manejo de errores y excepciones:

En el desarrollo de aplicaciones, es importante manejar los errores y excepciones que puedan ocurrir durante la ejecución del programa.

Puedes utilizar bloques try-catch para capturar y manejar excepciones. Por ejemplo:

```{csharp}

try
{
    // Código que puede generar una excepción
}
catch (Exception ex)
{
    Console.WriteLine("Ocurrió un error: " + ex.Message);
}
```
En este ejemplo, el código que puede generar una excepción se coloca dentro del bloque try, y si ocurre una excepción, se captura en el bloque catch y se muestra un mensaje de error en la consola.

## Almacenamiento de datos:

### Manejo de archivos para guardar y cargar información:

En .NET, puedes utilizar el manejo de archivos para guardar y cargar información en archivos en el sistema de archivos.

Para guardar información en un archivo, puedes utilizar la clase StreamWriter. Por ejemplo:

```{csharp}

using (StreamWriter archivo = new StreamWriter("datos.txt"))
{
    archivo.WriteLine("Hola, esto es un ejemplo de escritura en archivo.");
}
```
En este ejemplo, se crea un archivo llamado "datos.txt" y se escribe la línea de texto "Hola, esto es un ejemplo de escritura en archivo." en el archivo. La instrucción using asegura que el archivo se cierre correctamente después de su uso.

Para cargar información desde un archivo, puedes utilizar la clase StreamReader. Por ejemplo:

```{csharp}

using (StreamReader archivo = new StreamReader("datos.txt"))
{
    string contenido = archivo.ReadToEnd();
    Console.WriteLine(contenido);
}
```
En este ejemplo, se lee todo el contenido del archivo "datos.txt" utilizando el método ReadToEnd() y se muestra en la consola.

### Serialización y deserialización de objetos:

La serialización es el proceso de convertir un objeto en una secuencia de bytes para que pueda ser almacenado o transmitido, mientras que la deserialización es el proceso de reconstruir el objeto a partir de la secuencia de bytes.

En .NET, puedes utilizar la serialización XML o JSON para almacenar objetos en archivos o enviarlos a través de la red.

Para serializar un objeto en XML, puedes utilizar la clase XmlSerializer. Por ejemplo:

```{csharp}

// Clase de ejemplo
public class Persona
{
    public string Nombre { get; set; }
    public int Edad { get; set; }
}

// Serialización
Persona persona = new Persona { Nombre = "Juan", Edad = 25 };
XmlSerializer serializer = new XmlSerializer(typeof(Persona));
using (StreamWriter archivo = new StreamWriter("persona.xml"))
{
    serializer.Serialize(archivo, persona);
}
```
En este ejemplo, se crea una instancia de la clase Persona y se serializa en formato XML utilizando la clase XmlSerializer. El objeto serializado se guarda en el archivo "persona.xml".

Para deserializar un objeto desde XML, puedes utilizar el método Deserialize() de la clase XmlSerializer. Por ejemplo:

```{csharp}

// Deserialización
Persona personaDeserializada;
using (StreamReader archivo = new StreamReader("persona.xml"))
{
    personaDeserializada = (Persona)serializer.Deserialize(archivo);
}

Console.WriteLine($"Nombre: {personaDeserializada.Nombre}, Edad: {personaDeserializada.Edad}");
```
En este ejemplo, se lee el archivo "persona.xml" y se deserializa el objeto Persona utilizando el método Deserialize(). Luego, se muestra la información de la persona en la consola.

### Uso de bases de datos simples (opcional):

En .NET, puedes utilizar bases de datos simples como SQLite o SQL Server Compact Edition para almacenar y recuperar datos.

Puedes utilizar paquetes NuGet como System.Data.SQLite o EntityFramework.SqlServerCompact para trabajar con estas bases de datos.

El uso de bases de datos requiere una configuración adicional y la comprensión de conceptos como conexiones, consultas SQL, etc. Esta es una parte más avanzada del desarrollo y puede requerir un estudio más profundo.

## Implementación de la lógica de la aplicación:

### Desarrollo de métodos para agregar, modificar y eliminar tareas:

Define una clase Tarea que represente una tarea en tu aplicación. La clase puede tener propiedades como Id, Titulo, Descripcion, etc.

Crea una lista para almacenar las tareas en tu aplicación. Por ejemplo:

```{csharp}

List<Tarea> tareas = new List<Tarea>();
```
Para agregar una nueva tarea, puedes crear un método que solicite al usuario los datos de la tarea y los agregue a la lista. Por ejemplo:

```{csharp}

static void AgregarTarea()
{
    Console.WriteLine("Ingrese el título de la tarea:");
    string titulo = Console.ReadLine();
    
    Console.WriteLine("Ingrese la descripción de la tarea:");
    string descripcion = Console.ReadLine();
    
    // Generar un ID único para la tarea
    int id = GenerarIdUnico();
    
    Tarea nuevaTarea = new Tarea { Id = id, Titulo = titulo, Descripcion = descripcion };
    tareas.Add(nuevaTarea);
    
    Console.WriteLine("Tarea agregada con éxito.");
}
```
Para modificar una tarea existente, puedes crear un método que solicite al usuario el ID de la tarea y los nuevos datos a modificar. Por ejemplo:

```{csharp}

static void ModificarTarea()
{
    Console.WriteLine("Ingrese el ID de la tarea a modificar:");
    int id = int.Parse(Console.ReadLine());
    
    Tarea tarea = tareas.FirstOrDefault(t => t.Id == id);
    if (tarea != null)
    {
        Console.WriteLine("Ingrese el nuevo título de la tarea:");
        string nuevoTitulo = Console.ReadLine();
        
        Console.WriteLine("Ingrese la nueva descripción de la tarea:");
        string nuevaDescripcion = Console.ReadLine();
        
        tarea.Titulo = nuevoTitulo;
        tarea.Descripcion = nuevaDescripcion;
        
        Console.WriteLine("Tarea modificada con éxito.");
    }
    else
    {
        Console.WriteLine("No se encontró una tarea con ese ID.");
    }
}
```
Para eliminar una tarea, puedes crear un método que solicite al usuario el ID de la tarea y la elimine de la lista. Por ejemplo:

```{csharp}

    static void EliminarTarea()
    {
        Console.WriteLine("Ingrese el ID de la tarea a eliminar:");
        int id = int.Parse(Console.ReadLine());
        
        Tarea tarea = tareas.FirstOrDefault(t => t.Id == id);
        if (tarea != null)
        {
            tareas.Remove(tarea);
            Console.WriteLine("Tarea eliminada con éxito.");
        }
        else
        {
            Console.WriteLine("No se encontró una tarea con ese ID.");
        }
    }
```
Búsqueda y filtrado de tareas:

Puedes implementar métodos que permitan al usuario buscar tareas por título o descripción. Por ejemplo:

```{csharp}

    static void BuscarTareaPorTitulo()
    {
        Console.WriteLine("Ingrese el título de la tarea a buscar:");
        string titulo = Console.ReadLine();
        
        List<Tarea> tareasEncontradas = tareas.Where(t => t.Titulo.Contains(titulo)).ToList();
        
        if (tareasEncontradas.Count > 0)
        {
            Console.WriteLine("Tareas encontradas:");
            foreach (Tarea tarea in tareasEncontradas)
            {
                Console.WriteLine($"ID: {tarea.Id}, Título: {tarea.Titulo}, Descripción: {tarea.Descripcion}");
            }
        }
        else
        {
            Console.WriteLine("No se encontraron tareas con ese título.");
        }
    }
```
Puedes implementar métodos similares para buscar tareas por descripción u otros criterios.

### Marcar tareas como completadas:

Agrega una propiedad Completada a la clase Tarea para indicar si una tarea está completada o no. Por ejemplo:

```{csharp}

public bool Completada { get; set; }
```
Crea un método que permita al usuario marcar una tarea como completada. Por ejemplo:

```{csharp}

static void MarcarTareaComoCompletada()
{
    Console.WriteLine("Ingrese el ID de la tarea a marcar como completada:");
    int id = int.Parse(Console.ReadLine());
    
    Tarea tarea = tareas.FirstOrDefault(t => t.Id == id);
    if (tarea != null)
    {
        tarea.Completada = true;
        Console.WriteLine("Tarea marcada como completada.");
    }
    else
    {
        Console.WriteLine("No se encontró una tarea con ese ID.");
    }
}
```
## Pruebas unitarias

Creación de pruebas unitarias para verificar el correcto funcionamiento de los métodos:

### Uso de frameworks de pruebas como NUnit o XUnit:

Instala el framework de pruebas que prefieras en tu proyecto de .NET. Por ejemplo, puedes utilizar NUnit o XUnit.

Crea un proyecto de pruebas unitarias en tu solución. Puedes llamarlo "NombreProyecto.Tests" o cualquier otro nombre descriptivo.

Agrega referencias al framework de pruebas que estés utilizando. Por ejemplo, si estás utilizando NUnit, agrega la referencia a NUnit.Framework.

### Creación de pruebas unitarias:
Crea un archivo de pruebas, por ejemplo, NombreClaseTests.cs, en tu proyecto de pruebas unitarias.

Define una clase para tus pruebas y anótala con los atributos correspondientes del framework de pruebas. Por ejemplo, en 
NUnit:

```{csharp}

[TestFixture]
public class NombreClaseTests
{
    // Aquí se escribirán los métodos de prueba
}
```
Crea métodos de prueba para cada método que deseas probar en tu clase principal. Por ejemplo:

```{csharp}

[Test]
public void MetodoPrueba_DeberiaHacerAlgo()
    {
        // Configuración
        
        // Ejecución
        
        // Verificación de resultados
    }
```

Dentro de cada método de prueba, configura los datos necesarios, ejecuta el método que deseas probar y verifica los resultados esperados.

### Cobertura de pruebas y manejo de casos límite:

Asegúrate de cubrir diferentes escenarios y casos límite en tus pruebas unitarias. Esto implica probar diferentes combinaciones de datos de entrada, valores extremos y situaciones especiales.

Puedes utilizar aserciones (assertions) para verificar que los resultados obtenidos en las pruebas coincidan con los resultados esperados. Por ejemplo, en NUnit:

```{csharp}

[Test]
public void MetodoPrueba_DeberiaHacerAlgo()
{
    // Configuración
    
    // Ejecución
    
    // Verificación de resultados
    Assert.AreEqual(valorEsperado, resultadoObtenido);
}
```
Considera también el manejo de excepciones en tus pruebas. Puedes utilizar aserciones específicas para verificar que se lance una excepción en determinadas situaciones.

## Documentación y entrega:

### Comentarios en el código para explicar su funcionalidad:

Agrega comentarios en el código para explicar la funcionalidad de cada clase, método o sección relevante.

Utiliza comentarios claros y concisos para facilitar la comprensión del código a otras personas que lo lean en el futuro.

Comenta partes del código que sean complejas o que requieran una explicación adicional.

### Creación de un archivo README con instrucciones de compilación y ejecución:

Crea un archivo llamado "README.md" en la raíz de tu proyecto.

Proporciona una descripción general del proyecto, su propósito y las principales características.

Incluye instrucciones paso a paso sobre cómo compilar y ejecutar el proyecto.

Indica los requisitos previos, como la versión del SDK de .NET o las dependencias externas que se deben instalar.

Proporciona ejemplos claros de cómo utilizar el proyecto, con comandos o código de muestra cuando sea necesario.

Agrega cualquier otra información relevante, como la estructura de directorios, configuraciones especiales o recomendaciones adicionales.

### Empaquetado y entrega del proyecto final:

Antes de empaquetar el proyecto, asegúrate de haber probado y verificado su correcto funcionamiento.

Elimina cualquier archivo o carpeta innecesarios antes de la entrega, como archivos temporales, archivos de compilación o archivos de configuración local.

Si es necesario, asegúrate de incluir cualquier archivo adicional requerido para la ejecución del proyecto, como archivos de configuración o recursos externos.

Empaqueta el proyecto en un archivo comprimido (por ejemplo, un archivo ZIP) para facilitar su entrega.

Puedes utilizar herramientas de empaquetado específicas de .NET, como dotnet publish, para generar una versión compilada y lista para distribuir.