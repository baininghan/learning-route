## Java序列化

#### 什么是Java序列化
Java对象序列化是JDK1.1中引入的一组开创性特性之一，用于作为一种将Java对象的状态转换为字节数组，以便存储或传输的机制，以后，仍可以将字节数组转换回 Java 对象原有的状态。

实际上，序列化的思想是“冻结”对象状态，传输对象状态（写到磁盘、通过网络传输等等），然后“解冻”状态(反序列化)，重新获得可用的Java对象。所有这些事情的发生有点像是魔术，这要归功于ObjectInputStream/ObjectOutputStream类、完全保真的元数据以及程序员愿意用Serializable标识接口标记他们的类，从而 “参与” 这个过程。

新建一个`Person`类
```java
public class Person implements Serializable {

	private String name;
	private int age;
	
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
	
}
```
注意`Person`类，必须实现`Serializable`接口，然后进行测试。
```java
    public static void main(String[] args) {
		Person p = new Person();
		p.setName("Fancye");
		p.setAge(30);
		
		// 将Person对象序列化，写入perso.ser文件中
		try {
			FileOutputStream fos = new FileOutputStream("person.ser");
			ObjectOutputStream oos = new ObjectOutputStream(fos);
			oos.writeObject(p);
			
			oos.close();
			fos.close();
		} catch (FileNotFoundException e) {
			e.printStackTrace();
		} catch (IOException e) {
			e.printStackTrace();
		}
		
		// 从person.ser文件中反序列化，获取Person对象
		try {
			FileInputStream fis = new FileInputStream("person.ser");
			ObjectInputStream ois = new ObjectInputStream(fis);
			Person readP = (Person)ois.readObject();
			new File("person.ser").delete();
			
			System.out.println(readP.getName());
			System.out.println(readP.getAge());
		} catch (FileNotFoundException e) {
			e.printStackTrace();
		} catch (IOException e) {
			e.printStackTrace();
		} catch (ClassNotFoundException e) {
			e.printStackTrace();
		}
	}
```
先是实例化一个`Person`对象，姓名为`Fancye`，年龄为`30`。然后通过序列化的方式将`Person`对象`保存`到磁盘文件`person.ser`中。然后再通过反序列化的方式从磁盘文件`person.ser`中读取`Person`对象，控制台打印输出结果如下
```
Fancye
30
```
完美的`还原`了序列化之前对象`Person`的值。