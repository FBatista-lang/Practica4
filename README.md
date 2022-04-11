import java.sql.Connection;        
import java.sql.DriverManager;
import java.sql.SQLException;

import javax.swing.JOptionPane;


public class conexionOn {
    public static final String URL = "jdbc:mysql://localhost:3306/users";
    public static final String USER = "root";
    public static final String CLAVE = "";
    
   
    
    public static Connection conexion() {
     Connection conectar = null;
        try {
            Class.forName("com.mysql.jdbc.Driver");
            conectar = DriverManager.getConnection(URL, USER, CLAVE);
            
        } catch (ClassNotFoundException | SQLException e) {
            System.err.println(e.getLocalizedMessage());
        }
        return conectar;
    }//
    
    }
