
# Documentation collaborative

## IMIE 2017


- Ceci est une compilation de documents à des fins pédagogiques
- Réalisé avec les étudiants pour illustrer le travail collaboratif

### L'objet (classes et héritage)

### Visibilité des objets, classes et attributs

### Designs Patterns

### Swing

### Threads

### JDBC

### Fichiers
````Java
//Package à importer afin d'utiliser l'objet File
import java.io.File;

public class Main {
  public static void main(String[] args) {
    //Création de l'objet File
    File f = new File("test.txt");
    System.out.println("Chemin absolu du fichier : " + f.getAbsolutePath());
    System.out.println("Nom du fichier : " + f.getName());
    System.out.println("Est-ce qu'il existe ? " + f.exists());
    System.out.println("Est-ce un répertoire ? " + f.isDirectory());
    System.out.println("Est-ce un fichier ? " + f.isFile());
    System.out.println("Affichage des lecteurs à la racine du PC : ");
 
 for(File file : f.listRoots()){
      System.out.println(file.getAbsolutePath());
      try {
        int i = 1;  
        //On parcourt la liste des fichiers et répertoires
        for(File nom : file.listFiles()){
          //S'il s'agit d'un dossier, on ajoute un "/"
          System.out.print("\t\t" + ((nom.isDirectory()) ? nom.getName()+"/" : nom.getName()));
            if((i%4) == 0){
            System.out.print("\n");
          }
          i++;
        }
        System.out.println("\n");
      } catch (NullPointerException e) {
        //L'instruction peut générer une NullPointerException
        //s'il n'y a pas de sous-fichier !
      }
    }       
  }
}
````
Vous pouvez aussi effacer le fichier grâce la méthodedelete(), créer des répertoires avec la méthodemkdir()(le nom donné à ce répertoire ne pourra cependant pas contenir de point («.»)) etc.  

C'est par le biais des objets FileInputStream et FileOutputStream que nous allons pouvoir :

- lire dans un fichier ;
- écrire dans un fichier.

Ces classes héritent des classes abstraites InputStream et OutputStream, présentes dans le packagejava.io.

Comme vous l'avez sans doute deviné, il existe une hiérarchie de classes pour les traitementsinet une autre pour les traitementsout. Ne vous y trompez pas, les classes héritant d'InputStreamsont destinées à la lecture et les classes héritant d'OutputStreamse chargent de l'écriture !  

Sources : https://openclassrooms.com/courses/apprenez-a-programmer-en-java/les-flux-d-entree-sortie
