# Singleton
```java
public class SingletonLazyDoubleCheck {

	    private volatile static SingletonLazyDoubleCheck sc = null;
	    
	    private SingletonLazyDoubleCheck(){}
	    
	    public static SingletonLazyDoubleCheck getInstance(){
	        if(sc==null){
	            synchronized(SingletonLazyDoubleCheck.class){
	                if(sc==null){
	                    sc = new SingletonLazyDoubleCheck();
	                }  
	            }
	        }
	        return sc;
	    }
}
```
```java
public class SingletoneEnum {

	public enum SingleEnum{
		SINGLETON_ENUM;
	}
}
```
