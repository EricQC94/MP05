# Refacció

```
public class element {
    public int a;
    public String b;
}
```
```
public class programa {
    public static void main(String[] args) {
        element e1 = new element();
        e1.a = 11;
        e1.b = "Manuel Alfonseca";
        element e2 = new element();
        e2.a = 25;
        e2.b = "John Carmack";

        int aa = e1.a;
        int bb = e2.a;

        String z = " pot passar";

        if(!(aa<18)){
            System.out.println(e1.b+z);
        }else{if(!(aa>=18)){
            String y = " no ";
            System.out.println(e1.b+y+z);
        }}
        if(!(bb<18)){
            System.out.println(e2.b+z);
        }else{if(!(bb>=18)){
            String x = " no ";
            System.out.println(e2.b+x+z);
        }}
    }
}
```
