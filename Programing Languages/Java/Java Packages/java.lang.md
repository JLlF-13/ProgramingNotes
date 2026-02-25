This package is already improted in any java file

### Process & ProcessBuilder

`Process`:

`ProcessBuilder`: 

---
### Thread & Runnable

Both `Thread` and `Runnable` are used to create **concurrent processes** in Java — that means running multiple tasks at the same time.

- `Thread` is a class that represents a unit of execution.
    
- `Runnable` is an interface that defines a task to be executed by a thread.


> Each time you run them, the result may change — because threads run **concurrently**, and the order of execution is not guaranteed.
#### Thread

Parent File
```java
package Multifil.Ex1;

public class Exercsisi_2_1{
	public static void main(String[] args) throws InterruptedException{ 
		Fill1_2_1 h1 = new Fill1_2_1();
		Fill2_2_1 h2 = new Fill2_2_1();
		
		h1.start();
		h2.start();
		
		System.out.println("2 FILS INICIATS...");
	}
}
```

Child File 1
```java
package Multifil.Ex1;

public class Fill1_2_1 extends Thread{
	public void run() {
		while(true) {
			System.out.println("TIC");
			try {
				sleep(3000);
			} catch(InterruptedException e) {
				e.printStackTrace();
			}
		}
	}	
}
```

Child File 2
```java
package Multifil.Ex1;

public class Fill2_2_1 extends Thread{
	public void run() {
		while(true) {
		System.out.println("TAC");
			try {
				sleep(3000);
			} catch(InterruptedException e) {
				e.printStackTrace();
			}
		}
	}
}
```
#### Runnable

Parent File
```java
package Multifil.Ex2;

public class Exercisi_2_2{
	public static void main(String[] args){
		Fill1_2_2 h1 = new Fill1_2_2();
		Fill2_2_2 h2 = new Fill2_2_2();
		
		new Thread(h1).start();
		new Thread(h2).start();
		
		System.out.println("2 FILS INICIATS...");
	}
}
```

Child File 1
```java
package Multifil.Ex2;

public class Fill1_2_2 implements Runnable{
	public void run() {
		while(true) {
			System.out.println("TIC");
			try {
				Thread.sleep(2000);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}	
	}
}
```

Child File 2
```java
package Multifil.Ex2;

public class Fill2_2_2 implements Runnable{
	public void run() {
		while(true) {
			System.out.println("TAC");
			try {
				Thread.sleep(2000);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}	
	}
}
```