1. Print in python is as simple as writing english

   print("Hello world!")

   Also comments in python is #. write '#' before your text and this is a comment

2. Data types in Python
   1. str, int, float, bool, list(array), dict(object), set(unique values), tuple(locked list)
   2. data types can be changed. Like,
      1. x = 1
         print(x) //output: 1
      2. x = "the same variable but different data type"
         print(x) //output: the same variable but different data type

3. Methods
   1. is like functinons to work with data type like for strings there are upper(), lower(), title(). some others are
      1. "Hellow World".count('l') counts number of time 'l' appears in the string. takes 1 parameter
      1. "Hellow World".replace('o', 'u') replaces given string with the updating string. takes 2 parameters

4. Variables
   1. text1 = "this is how we can create the variable"
   2. Naming rules:
      1. This is allowed:
         1. \_name = "ok"
         2. my_var = 10
         3. age2 = 25
      2. this is not allowed:
         1. 2age = 16
         2. my-var = "not_ok"

   3. Variables can be exchanged without using a third variable
      1. a = 5
      2. b = 6
      3. a, b = b, a; // now a = 6, b = 5

   4. To check the datatype of variable we can use type() function. {type(variable_name)}
   5. Multiple assignments: a, b, c = 12, 56, 75;
   6. Reserved keywords: if, else, for, while, class, def, True, False
   7. Python variables are references not boxes.

5. List (array in python): We can declare lists using braces. They can contain any datatype or mixed datatype. These are ordered, mutable collection.

   1. list1 = [1, "hello", True, 3.5]

   2. Indexing: 0 and negative indexing
      1. list1[0] # 1
      2. list1[-1] # 3.5

   3. Slicing: lst[23, 45, 37, 12, 78]
      1. lst[1:4] # 45, 37, 12
      2. lst[:3] # 23, 45, 37
      3. lst[::2] # 23, 37, 78

   4.  Modify list:
      1. lst[0] = 100 # [100, 45, 37, 12, 78]

   5.  Add elements:
        1. list2 = [1, 2]
           1. list2.append(3) # [1, 2, 3]
           2. list2.insert(1, 99) # [1, 99, 2, 3]
           3. list2.extend([200, 300]) #[1, 99, 2, 3, 200, 300]

   6.  Remove Elements:
        1. list2.remove(2) #removes first 2 elements of the list
        2. list2.pop() #removes the last element
        3. list2.pop(2) #removes the element of index of 2
        4.  del.list[0] #delete index
        5.  list.clear() empties the list

   7.  Identity vs Equality
        1. a = [1, 2]
         b = [1, 2]

        2. print(a == b) # True (values same)
         print(a is b) # False (different objects)

   8.  Looping

       1. for x in list:
         print(x);
   
       2.  (with Index:-) for i in range (len(list)): print(list[i])
   
       3.  (best:-) for i, val in enumerate(list):  print(i, val)

   9.  list length

        1.  len(lst)

   10. membership check:- if 2 in lst: print ("yes")
   
   11. Sorting:-
       
       1.  list.sort()     #mutates the original list
       2.  sorted.(list)   #returns a new list without mutating the original list
       3.  lst.sort(reverse: True)  #mutates the orighinal list, sorting in descinding order
   
   12. Copy:- 
       
       1.  a.copy() or b = a[:]
       2.  b = a        #same refernece not a copy
   
   13. Nested list:-
       
       1.  list = [[1,2], [3,4]]
       2.  lst[0][1]    #Output: 1
   
   14. List comprehension:-
       
       1.  lst = [x*x for x in range(5)]
       2.  lst = [x for x in range(10) if x % 2 == 0]
   
   15. Built in function:-
       1.  min(lst)
       2.  max(lst)
       3.  sum(lst)

6.  
