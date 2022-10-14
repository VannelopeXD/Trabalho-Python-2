# Trabalho-Python-2

from ctypes import pointer
from re import A
from signal import valid_signals
from node import Node


class Linkedilist:
    def __init__(self):
        self.head = None
        self._size = 0

        def append (self,elem):
            if self.head:
                pointer = self.head
                while(pointer.next):
                    pointer = pointer.next
                pointer.next = Node(elem)
            else:

                self.head = Node(elem)
            self._size = self._size + 1
           
        def __len__(self):
            return self._size

            def get(self,index):
                pass
        def set (self,index,elem):
            pass

        def __getitem__(self,index):
            
            pointer = self.head
            for i in range(index):
                if pointer:
                    pointer.pointer.next
                else:
                    raise IndexError("list index out of range")
            if pointer:
                return pointer.data
            raise IndexError("list index out of range")

        def __setitem__(self,index,elem):
            
            #lista[5] = 9
            pointer = self.head
            for i in range (index):
                if pointer:
                    pointer = pointer.next
                else:
                    raise IndexError("list index out of range")
            if pointer:
                pointer.data = elem
            else:
                raise IndexError("list index out of range")

        def index(self,elem):
            """retorna o indice do elemento na lista"""
            pointer = self.head
            i = 0
            while(pointer):
                if pointer.data == elem:
                    return i 
                pointer = pointer.next
                i = i+1
            raise ValueError ("{} is not in list".format(elem))

        #inserir elementos no começo da lista
        def insert(self,index,elem):
             if index == 0:
                node = Node(elem)
                node.next = self.head
                self.head = Node

                else:
                pointer = self.head
                for i in range (index):
                    if pointer:
                        pointer = pointer.next
                    else:
                        raise IndexError("list index out of range")


    lista = Linkedilist = 0
    lista.append(7)
    lista.append(80)

    
