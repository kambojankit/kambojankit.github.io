---
layout: single
title:  "Data Structures"
header:
  teaser: "unsplash-gallery-image-2-th.jpg"
categories:
  - Jekyll
tags:
  - edge case
---


+ Arrays

  - Contiguous area of memory consisting of equal size elements indexed by Contiguous integers
  - Constant time access to the elements
  - constant time to add or remove the elements
  - Linear time to add or remove at any arbitrary  location.
  -

  -  1-D
      elem_addr + element_size(i-first_index)
  -  2-Dimensional
      elem_addr + element_size * ((row_index - initial_row_index) * (row_size) + (column_index-initial_column_index))

      + Row major
      + column major

  -Common Operations

    __________  Add __|__ Remove
    Beginning | O(n)  | O(n)
          End | O(1)  | O(1)
       Middle | O(n)  | O(n)

+ Linked List

    Node
      Key
      next pointer

    List API (order of operations are calculated, assuming no tail pointer is present.)

      PushFront(key)        O(1), add an element to the Front of the list, so it takes the key and adds it to the front.
      Key TopFront()        O(1), return front item of the list
      PopFront()            O(1), remove front element of the list

      PushBack(Key)         O(n), add an element to the back of the list, so it takes the key and adds it to the end/back, a.k.a Append
                                 Operation.  (with tail pointer its an O(1) operation.)
      Key TopBack()         O(n), return last/back item of the list  (O(n), even with tail pointer)
      PopBack()             O(n), remove last/back element of the list  (O(n), even with tail pointer)

      Boolean Find(key)     O(n), is Key in the List?
      Erase(Key)            O(n), remove Key from the list.

      Boolean Empty()       O(1), check if list is empty or not?

      AddBefore(Node,Key)   O(n), adds key before the node.
      AddAfter(Node,Key)    O(n), adds key after the node.

 +  PushFront(key)
      node <- new Node
      node.key <- key
      node.next <- head
      head <- node
      if tail == nil
         tail <- head

 +  PopFront()
     if head = nil
        ERROR: empty list
     head <- head.next
     if head = nil
        tail <- nil

 +  PushBack(key)
     node <- new node
     node.key <- key
     node.next = nil

     if tail = nil
       head <- tail <- nil
     else
      tail.next <- node
      tail <- node

  + PopBack()
      if head = nil
          Error: empty list
      if head = tail
          head <- tail <- nil
      else
         p <- head
         while p.next.next != nil
           p <- p.next

         p.next <- nil; tail <- p;

   + AddAfter()
      node2 <- new node;
      node2.key <- key
      node2.next <- node.next
      node.next  = node2
      if tail = node
         tail <- node2


+ Double Linked List
  + Do a detailed discussion on the Doubly Linked list.
