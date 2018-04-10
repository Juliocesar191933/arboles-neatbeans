# arboles-neatbeans
ackage arboles;

public class Pruebaarbol {

     public static void main(String[] args) {
    Nodo raiz = new Nodo(18);
    Nodo nodo2 = new Nodo(22);
    Nodo nodo3 = new Nodo(16);
    Nodo nodo4 =new Nodo(15);

    
    nodo3.setNodoIzquierdo(new Nodo(12));
    nodo3.setNodoDerecho(new Nodo(10));  

    nodo4.setNodoIzquierdo(new Nodo(6));

    nodo2.setNodoIzquierdo(nodo4);
    nodo2.setNodoDerecho(new Nodo(14));
      
    raiz.setNodoIzquierdo(nodo2);
    raiz.setNodoDerecho(nodo3);

    System.out.println("Recorrido Preorden: ");
    preOrden(raiz);
    System.out.println("\nRecorrido Inorden: ");
    inorden(raiz);
    System.out.println("\nRecorrido Postorden: ");
    posOrden(raiz);
  }
 
  private static void preOrden(Nodo raiz) {
    if (raiz != null) {
      System.out.print(" "+raiz.getDato());
      preOrden(raiz.getNodoIzquierdo());
      preOrden(raiz.getNodoDerecho());
    }
  }
 

  private static void inorden(Nodo raiz) {
    if (raiz != null) {
      inorden(raiz.getNodoIzquierdo());
      System.out.print("  "+raiz.getDato());
      inorden(raiz.getNodoDerecho());
    }
  }
 

  private static void posOrden(Nodo raiz) {
    if (raiz != null) {
      posOrden(raiz.getNodoIzquierdo());
      posOrden(raiz.getNodoDerecho());
      System.out.print("  "+ raiz.getDato() );
    }
  }

}
