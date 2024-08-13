// Java Program to implement a FIFO-based Queue 
import java.util.*; 
import java.util.Queue; 

class MyQueue { 
	// Store Elements 
	private List<Integer> data;		 
	private int p_start;			 
	public MyQueue() { 
		data = new ArrayList<Integer>(); 
		p_start = 0; 
	} 
	public boolean enQueue(int x) { 
		data.add(x); 
		return true; 
	};	 
	
	// Delete the item from queue 
	public boolean deQueue() { 
		if (isEmpty() == true) { 
			return false; 
		} 
		p_start++; 
		return true; 
	} 
	
	// Find the first item from the queue 
	public int Front() { 
		return data.get(p_start); 
	} 
	public boolean isEmpty() { 
		return p_start >= data.size(); 
	}	 
}; 

// Driver Class 
public class Main { 
	// Main Function 
	public static void main(String[] args) { 
		MyQueue q = new MyQueue(); 
		q.enQueue(5); 
		q.enQueue(3); 
		
		if (q.isEmpty() == false) { 
			System.out.println(q.Front()); 
		} 
		q.deQueue(); 
		if (q.isEmpty() == false) { 
			System.out.println(q.Front()); 
		} 
		q.deQueue(); 
		if (q.isEmpty() == false) { 
			System.out.println(q.Front()); 
		} 
	} 
}
