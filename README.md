# Queues-Operations-Using-Array
Operations:- add, remove, find peek etc.

// # code
public class Moving
{
 static class Q
    {
      static int [] arr;
      static int size;
      static int rear;  
      Q(int n)
      {
          arr = new int[n];
          size =n;
          rear=-1;
      }
    
    public static boolean isEmpty()
    {
        return rear == -1;
    }
    public static void add(int data)
    {
        if(rear==size-1)
        {
            System.out.println("Queue is Full");
            return;
        }
        
            rear = rear+1;
            arr[rear]=data;
      
    }
    public static int remove()
    {
        if(isEmpty())
        {
            System.out.println("Queue is Empty");
            return -1;
        }
       
            int front = arr[0];
            for(int i=0; i<rear; i++)
            {
                arr[i]=arr[i+1];
            }
            rear=rear-1;
            return front;
        
    }
    public static int peek()
    {
         if(isEmpty())
        {
            System.out.println("Queue is Empty");
            return -1;
        }
        return arr[0];
        
    }
    
    }
    public static void main(String [] args)
    {
        Q q = new Q(5);
        q.add(1);
        q.add(2);
        q.add(3);
        while(!q.isEmpty())
        {
            System.out.println(q.peek());
            q.remove();
        }
       
    }
}

