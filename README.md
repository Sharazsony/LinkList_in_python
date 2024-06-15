# LinkList_in_python
class Node:
   def __init__(self,d=None,n=None):
       self.data=d 
       self.next=n
class List:
   def __init__(self):
       self.head=None
   def add(self,data):
       node=Node(data)
       if self.head is None:
           
           self.head=node
       else:
           i=self.head
           while i.next!=None:
               i=i.next
               node=Node(data)
           i.next=node  
   def Del(self):
       cur=self.head
       Nex=cur.next
       while Nex.next!= None:
                print("del:",Nex.data)
                cur=cur.next
                Nex=Nex.next
       cur.next=None        
                      
   def print(self):
        i=self.head
        while i != None:
                print(i.data)
                i=i.next
                 
linked_list = List()
linked_list.add(1)
linked_list.add(2)
print("before delegation: ")
linked_list.print()
print("After delegation: ")
linked_list.Del()
linked_list.print()
