# curso
programadores
package biblioteca;
  import java.sql.Connection;
import java.sql.DriverManager;
  import java.sql.SQLException;
public class Conexion {
	public static void main(String[] args) {
	}Connection con; 
		private String DRIVER = "com.mysql.cj.jdbc.Driver";
		private String BD_URL= "jdbc:mysql://localhost:3306/bd_ejemplo";
		private String USER = "root";
		private String PASS = "";
		public Connection conectar() {
			Connection conexion=null;
		try {
		Class.forName("DRIVER");	
	  con = DriverManager.getConnection(BD_URL,USER,PASS);
		System.out.println("conexion ok");
	} catch (ClassNotFoundException e) {
		System.out.println("error al establecer conexion");
		e.printStackTrace();
	}catch(SQLException e) {
		System.out.println("error en la conexion");
		e.printStackTrace();
	}
		return con;
	}
		
