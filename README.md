#Profesor-Alumno
namespace Profes
{
    internal class Alumno
    {
        private int nl;
        private string nombre;
        private ArrayList materias = new ArrayList();
        private ArrayList calificaciones = new ArrayList();

        public int Nl { get => nl; set => nl = value; }
        public string Nombre { get => nombre; set => nombre = value; }
        public ArrayList Materias { get => materias; set => materias = value; }
        public ArrayList Calificaciones { get => calificaciones; set => calificaciones = value; }
        public void agregarMaterias(string materia)
        {
            materias.Add(materia);
        }
        public void agregarCalificaciones(int calificacion)
        {
            calificaciones.Add(calificacion);
        }
    }
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
