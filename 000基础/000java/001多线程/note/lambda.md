# lambda

![](../img/lambda-1.png)

```java
public class TestLambda {

    static class Like2 implements Ilike{
        public void lambda(){
            System.out.println("lambda2");
        }
    }

    public static void main(String[] args) {
    Ilike like=new Like();
    like.lambda();

    like =new Like2();
    like.lambda();

    class Like3 implements Ilike{
        public void lambda(){
            System.out.println("lambda3");
        }
    }

    like = new Like3();
    like.lambda();

        //********************************
    like =()->{
        System.out.println("lambda4");
    };
    like.lambda();
//******************************************
    }
}

interface Ilike{
    void lambda();
}
class Like implements Ilike{
    public void lambda(){
        System.out.println("lambda");
    }
}
```

## 有参

```java
interface Ilike{
    void lambda(int a);
}
class Like implements Ilike{
    public void lambda(int a){
        System.out.println("lambda");
    }
}

//==================================


main(){
    
    Ilike like =a->System.out.println("lambda");
    
    //如果有两个参数
    like = (a,b)->{
        sout("xxxxx"+a);
        sout("xxxxx"+b);
    }
    
    
    
    
}

```

