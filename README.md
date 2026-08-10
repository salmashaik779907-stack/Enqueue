# Enqueue
Enqueue – Adds an element to the rear/end of a queue.
import java.util.Queue;
class Queues
{
    int arr[];
    int front,rear,size;
    Queues(int size)
    {
        this.size=size;
        arr=new int[size];
        front=0;
        rear=-1;
    }
    //insert
    public void enqueue(int value)
    {
        if(rear==size-1)
        {
            System.out.println("It is not empty");
            return;
        }
        arr[++rear]=value;
        System.out.println(value+"all are inserted");
    }
    public void display()
    {
        if(front>rear)
        {
            System.out.println("empty");
            return;
        }
        for(int i=front;i<=rear;i++)
        {
            System.out.println(arr[i]+" ");
        }
        System.out.println();
    }
    public static void main(String args[])
    {
        Queues q=new Queues(5);
        q.enqueue(10);
        q.enqueue(20);
        q.enqueue(30);
        q.enqueue(40);
        q.enqueue(50);
        q.display();
    }
}
