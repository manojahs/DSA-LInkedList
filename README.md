# DSA-LInkedList

<img width="482" height="230" alt="image" src="https://github.com/user-attachments/assets/b2e83af4-d261-43c1-b80e-1231d1283b60" />
<img width="508" height="278" alt="image" src="https://github.com/user-attachments/assets/492754cf-03f2-4e5d-af29-e2993dfbd87a" />
<img width="484" height="278" alt="image" src="https://github.com/user-attachments/assets/0208b1da-a23b-4e01-ba34-8b092ef19f54" />
<img width="473" height="233" alt="image" src="https://github.com/user-attachments/assets/fc0bf82e-9bd4-4bcb-861d-4ae6b4046072" />
<img width="506" height="260" alt="image" src="https://github.com/user-attachments/assets/14a48914-c2ce-4467-a97d-bd144ad66026" />
<img width="485" height="281" alt="image" src="https://github.com/user-attachments/assets/e0d67f9c-15ce-4d0d-b4d2-34712c0f85b5" />



```
Array
---------

Blocks the sequential Memory starts with first element with 0 index

Limitations of an array
1)Array stored only same datatype values
2)Array is having fixed amount of size it cannot be changed

Linked List
-------------
1)Linked list is a collection of elements where each elements represented as Node
2)Node is the computer location in the memory it contains like data and Next
3)Link which stored the address of another Node

Linked List Traverse and Display
---------------------------------
// See https://aka.ms/new-console-template for more information
using System;
using System.Reflection.Metadata.Ecma335;


public class Node
{
    public int Element;
    public Node Next;

    public Node(int e , Node node)
    {
        Element = e;
        Next = node;
    }
}

public class  LinkedList
{
    private Node head;
    private Node Tail;
    private int size;

    public LinkedList()
    {
        head = null;
        Tail = null;
        size = 0;
    }

    public int Length()
    {
        return size;
    }

    public bool IsEmpty()
    {
        return size == 0;
    }

    public void AddLast(int e)
    {
        Node newest = new Node(e, null);
        if (IsEmpty())
        {
            head = newest;
        }
        else
        {
            Tail.Next = newest;
        }
        Tail = newest;
        size += 1;
    }

    public void Display()
    {
        Node p = head;
        while(p!=null)
        {
            Console.Write(p.Element + " ");
            p = p.Next;
        }
        Console.WriteLine();
    }

    public static void Main()
    {
        LinkedList list= new LinkedList();
        list.AddLast(10);
        list.AddLast(20);
        list.AddLast(30);
        list.Display();  // 10 20 30
        Console.WriteLine("Size is" + list.Length()); //Size is 3

    }
    
}



```
