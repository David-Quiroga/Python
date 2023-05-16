class Persona {
    public  nombre        :string;
    public  identificacion:string;
    public  edad          :number;
    public  direccion     :string;

    constructor (nombre : string, identificacion:string, edad:number, direccion:string){
        this.nombre = nombre;
        this.identificacion = identificacion;
        this.edad = edad;
        this.direccion = direccion
    }
    saludar(){
        console.log("Mi nombre es " + this.nombre + " y tengo " + this.edad )
        console.log("Soy estudiante de la carrera de software")
    }
}

class Estudiante extends Persona{
    public numeroMatricula : number
    public nivel   : string;
    
    constructor(nombre:string, identificacion:string,edad:number,direccion:string, numeroMatricula:number, nivel:string){
        super(nombre,identificacion,edad,direccion);
        this.numeroMatricula = numeroMatricula;
        this.nivel           = nivel;

    }

}

class Docente extends Persona {
    public contrato : string;
    public titulo   : string;
    constructor(nombre:string, identificacion:string,edad:number,direccion:string,contrato : string, titulo:string){
        super(nombre,identificacion,edad,direccion);
        this.contrato = contrato;
        this.titulo = titulo
    }
}

//let estudiante1 = new Estudiante(1,"Tercero");
//console.log(estudiante1.numeroMatricula,estudiante1.nivel)
//document.write(estudiante1.numeroMatricula,estudiante1.nivel)

//let docente1    = new Docente ("definodo","Master")
//console.log(docente1.contrato, docente1.titulo)

let persona1 = new Persona("David","987879",22,"Ecuatoriana")
console.log(persona1.saludar())

class Empleado {
    public nombre: string;
    public horasTrabajadas: number;
    public salarioPorHora: number;

    constructor(nombre: string, horasTrabajadas: number, salarioPorHora: number) {
        this.nombre = nombre;
        this.horasTrabajadas = horasTrabajadas;
        this.salarioPorHora = salarioPorHora;
    }
    public calcularSueldo(): number {
      return this.horasTrabajadas * this.salarioPorHora;
    }
}

const empleado1 = new Empleado("Juan", 500, 20);
console.log(`El sueldo de ${empleado1.nombre} es: ${empleado1.calcularSueldo()}`);

const empleado2 = new Empleado("María", 30, 15);
console.log(`El sueldo de ${empleado2.nombre} es: ${empleado2.calcularSueldo()}`);

//instancias

interface Vehiculo {
    modelo:string;
    fabricante:string;
    encender(): void;
    detener(): void;
    acelerar(): void;
}

interface vehiculoTerrestre extends Vehiculo {
    numeroLlantas:number;
    conducir(): void;
}

interface vehiculoMaritimo extends Vehiculo {
    numeroAnclas:number;
    navegar(): void;
}

interface vehiculoAereo extends Vehiculo {
    numeroTurbinas:number;
    pilotar(): void;
}
    


class Camioneta implements vehiculoTerrestre {
    modelo:string = "4x4";
    fabricante:string = "Casa Vaca";
    numeroLlantas?:number;
    placa:number;
    encender(): void;
    detener(): void;
    acelerar(): void;
    conducir(): void;
}

class Submarino implements vehiculoMaritimo {
    modelo:string;
    fabricante:string;
    numeroAnclas:number = 0;
    navegar(): void;
    conducir(): void;
    encender(): void;
    detener(): void;
    acelerar(): void;
}

class Helicoptero implements vehiculoAoreo {
    modelo:string;
    fabricante:string;
    encender(): void;
    detener(): void;
    acelerar(): void;
    numeroTurbinas:number;
    pilotar(): void;
}

interface Animal {
  nombre: string;
  tipo: string;
}

class Perro implements Animal {
  nombre: string;
  tipo: string;
  raza: string;

  constructor(nombre: string, tipo: string, raza: string) {
    this.nombre = nombre;
    this.tipo = tipo;
    this.raza = raza;
  }
}

// Ejemplo de uso
const miPerro = new Perro("Fido", "Mamífero", "Golden Retriever");
console.log(miPerro.nombre); // Fido
console.log(miPerro.tipo); // Mamífero
console.log(miPerro.raza); // Golden Retriever

