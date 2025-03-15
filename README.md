using Profes;

using System.Data;

Dictionary<string, string> diccionario = new Dictionary<string, string>();

Profesor prof = new Profesor();
Console.WriteLine("Nombre del Profesor: ");
prof.NombreProf = Console.ReadLine();
Console.WriteLine("Ingrese los datos del alumno");
prof.capturarDatosAlumno();
prof.capturarMaterias();
prof.capturarCalificaciones();


Console.WriteLine("\n******...DATOS:...******");
Console.WriteLine("Profesor: " + prof.NombreProf);
Console.WriteLine("\n-----Datos alumno:----- ");
Console.WriteLine("NL: " + prof.Alumno1.Nl);
Console.WriteLine("Nombre del alumno: " + prof.Alumno1.Nombre);
Console.WriteLine("\n-----Materias-----");


for (int i = 0; i < prof.Alumno1.Materias.Count; i++)
{
    diccionario.Add(prof.Alumno1.Materias[i].ToString(), prof.Alumno1.Calificaciones[i].ToString());

}

foreach (var elementos in diccionario)
    Console.WriteLine(elementos.ToString());

foreach (string clave in diccionario.Keys)
{ Console.WriteLine(clave); }

foreach (string valor in diccionario.Values)
{ Console.WriteLine(valor); }
