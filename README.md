#Profesor-Alumno
namespace Profes
{
    internal class Profesor
    {
        private String nombreprof;
        private Alumno alumnito = new Alumno();

        public string NombreProf { get => nombreprof; set => nombreprof = value; }
        internal Alumno Alumno1 { get => alumnito; set => alumnito = value; }
        public void capturarDatosAlumno()
        {
            string nombre;
            int nl;
            Console.WriteLine("NL: ");
            nl = Convert.ToInt16(Console.ReadLine());
            Console.WriteLine("Nombre: ");
            nombre = Console.ReadLine();
            alumnito.Nl = nl;
            alumnito.Nombre = nombre;

        }
        public void capturarMaterias()
        {
            string materia;
            for (int i = 0; i < 7; i++)
            {

                Console.WriteLine("Ingrese Materia: ");
                materia = Console.ReadLine();
                alumnito.agregarMaterias(materia);
            }
        }

        public void capturarCalificaciones()
        {
            int calificacion;
            for (int i = 0; i < 7; i++)
            {
                Console.WriteLine("Calificacion de " + alumnito.Materias[i]);
                calificacion = Convert.ToInt32(Console.ReadLine());
                alumnito.agregarCalificaciones(calificacion);
            }
        }
    }
}
