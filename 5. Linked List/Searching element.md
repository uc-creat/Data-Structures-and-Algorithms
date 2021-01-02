## Searching:

create a linked list:

```py

class node:
    __slots__ = 'data', 'addr'
    
    def __init__(self, data, addr):
        self.data = data
        self.addr = addr
        
class linked_list:
    def __init__(self):
        self.head = None
        self.tail = None
        self.size = 0
        
    def __len__(self):
        return self.size
        
    def add(self, data):
        newnode = node(data, None)
        if self.size == 0:
            self.head = newnode
        else:
            self.tail.addr = newnode
        self.tail = newnode
        self.size += 1
        
# searching the position of the element e:

    def search(self, e):
        p = self.head
        i = 0
        while p:
            if p.data == e:
                print(i)
            else:
                p = p.addr
                i += 1
        return('not found')
            

```

Here, we are simply traversing the list, using a while loop.
first we make a 
