# Singleton

```java
import java.io.*;

class Untitled {
	public static void main(String[] args) {
		System.out.print("Hello\n");
		System.out.print(EasySingleton.INSTANCE.getName());
		System.out.print(EasySingleton.INSTANCE.getName());
		System.out.print(EasySingleton.INSTANCE.getName());
	}
	
	public enum EasySingleton{
		INSTANCE;
		int count = 0;
		public String getName() {
			count++;
			return "Singleton " + count + "\n";
		}		
	}
}
```


