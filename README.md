
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet (classes et héritage)

Bonjour les amis !

### Visibilité des objets, classes et attributs

Comment ça va ?

### Designs Patterns

### Swing

Développement d'interfaces graphiques :

Classes Jframe :
  exemple de code :
  
  ------------------------------------------
  import javax.swing.*;
   
  public class TestJFrame1 { 
    public static void main(String argv[]) 
      JFrame f = new JFrame("ma fenetre");
      f.setSize(300,100);
      f.setVisible(true);
    }
  }
  -----------------------------------------
  
  
  
  Utilisation du GetContentPane avec ajout d'un bouton:
  
  ----------------------------------------
  import javax.swing.*;

  public class TestJFrame2 {
     public static void main(String argv[]) {

       JFrame f = new JFrame("ma fenetre");
       f.setSize(300,100);
       JButton b =new JButton("Mon bouton");
       f.getContentPane().add(b);
       f.setVisible(true);
    }
  }
  -----------------------------------------
  
  
  
  Création d'un menu : 
  
  -----------------------------------------
  import javax.swing.*;
  import java.awt.*;


public class TestJFrame6 {
    public static void main(String argv[]) { 

       JFrame f = new JFrame("ma fenetre");
       f.setSize(300,100);
       JButton b =new JButton("Mon bouton");
       f.getContentPane().add(b);
       JMenuBar menuBar = new JMenuBar();
       f.setJMenuBar(menuBar);
       JMenu menu = new JMenu("Fichier");
       menu.add(menuItem);
       menuBar.add(menu);
       f.setVisible(true);

   }
}
 

### Threads

### JDBC

### Fichiers
