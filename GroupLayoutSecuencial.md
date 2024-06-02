import javax.swing.GroupLayout;
import javax.swing.JButton;
import javax.swing.JFrame;
public class GroupLayoutSecuencial {
    public static void main(String[] args) {
        // Crear un JFrame para la ventana principal
        JFrame frame = new JFrame("Ejemplo GroupLayout Secuencial");
        frame.setBounds(0,0,350,150);
        frame.setResizable(false);
        frame.setLocationRelativeTo(null);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        // Crear componentes (botones)
        JButton button1 = new JButton("Botón 1");
        JButton button2 = new JButton("Botón 2");
        JButton button3 = new JButton("Botón 3");
        // Crear un GroupLayout y establecerlo en el panel de contenido del JFrame
        GroupLayout layout = new GroupLayout(frame.getContentPane());
        // Establecer el GroupLayout como administrador de diseño del panel de contenido del JFrame
        frame.getContentPane().setLayout(layout);
        // Configurar el GroupLayout secuencialmente (horizontalmente)
        layout.setHorizontalGroup(
            layout.createSequentialGroup() // Inicia una secuencia horizontal
                .addComponent(button1) // Agrega el botón 1
                .addComponent(button2) // Agrega el botón 2
                .addComponent(button3) // Agrega el botón 3
        );
        // Configurar el GroupLayout secuencialmente (verticalmente)
        layout.setVerticalGroup(
            layout.createParallelGroup(GroupLayout.Alignment.BASELINE) // Inicia una secuencia vertical alineada en la base
                .addComponent(button1) // Agrega el botón 1
                .addComponent(button2) // Agrega el botón 2
                .addComponent(button3) // Agrega el botón 3
        );
        // Ajusta automáticamente el tamaño del JFrame para que quepa todos los componentes
        frame.pack();
        // Hace visible el JFrame
        frame.setVisible(true);
    }
}
