# Mini-Projects
def listoperations(mylist):
    while True:
        print("""\nList Operations:
        1. About lists
        2. Print List
        3. Append Element
        4. Insert List
        5. Remove Element
        6. Index of Element
        7. Reverse List
        8. Clear List
        9. Return to Main Menu""")

        choice = int(input("Enter your choice (1-9): "))
        if choice == 1:
            print("DEF: A list is built in mutable,inordered,heterogenious,sequence of elements.")
        elif choice == 2:
            print("List:", mylist)
        elif choice == 3:
            Element_To_Append = input("Enter an element to append to the list: ")
            mylist.append(Element_To_Append)
            print("After Append:", mylist)
        elif choice ==4:
            Index_To_Insert = int(input("Enter an index to insert the element: "))
            Element_To_Insert = input("Enter an element to insert into the list: ")
            mylist.insert(Index_To_Insert, Element_To_Insert)
            print("After Insert:", mylist)
        elif choice == 5:
            Element_To_Remove = input("Enter an element to remove from the list: ")
            try:
                mylist.remove(Element_To_Remove)
                print("After Remove:", mylist)
            except ValueError:
                print("Element not found in list!")
        elif choice == 6:
            Element_To_Find = input("Enter an element to find its index: ")
            try:
                index = mylist.index(Element_To_Find)
                print("Index of {}: {}".format(Element_To_Find, index))
            except ValueError:
                print("{} not found in list!".format(Element_To_Find))
        elif choice == 7:
            mylist.reverse()
            print("Reversed List:",mylist)
        elif choice == 8:
            mylist.clear()
            print("List Cleared.")
        elif choice == 9:
            print("Returning to Main Menu.")
            break
        else:
            print("Invalid choice....Please enter a number between 1 and 9....")


def tupleoperations(mytuple):
    while True:
        print("""\nTuple Operations:
        1. About Tuple
        2. Print Tuple
        3. Access Element
        4. Concatenate Tuples
        5. Return to Main Menu""")

        choice = int(input("Enter your choice (1-5): "))
        if choice ==1:
            print("DEF :A tuple is a built in immutable,inoredered,heterogenious sequence of elements. ")
        elif choice == 2:
            print("Tuple:", mytuple)
        elif choice == 3:
            index_to_access = int(input("Enter an index to access from the tuple: "))
            try:
                accessed_element = mytuple[index_to_access]
                print("Accessed Element:", accessed_element)
            except IndexError:
                print("Index out of range!!")
        elif choice == 4:
            another_tuple = tuple(input("Enter elements for another tuple (separated by comma): ").split(','))
            concatenated_tuple = mytuple + another_tuple
            print("Concatenated Tuple:", concatenated_tuple)
        elif choice == 5:
            print("Returning to Main Menu.")
            break
        else:
            print("Invalid choice... Please enter a number between 1 and 5...")


def setoperations(myset):
    while True:
        print("""\nSet Operations:
        1. About set
        2. Print Set
        3. Add Element
        4. Remove Element
        5. Clear Set
        6. Return to Main Menu""")

        choice = int(input("Enter your choice (1-6): "))
        if choice == 1:
            print('''DEF: A Set is a built in unordered collection of unique elements.''')
        elif choice == 2:
            print("Set:", myset)
        elif choice == 3:
            element_to_add = input("Enter an element to add to the set: ")
            myset.add(element_to_add)
            print("After Adding Element:", myset)
        elif choice == 4:
            element_to_remove = input("Enter an element to remove from the set: ")
            try:
                myset.remove(element_to_remove)
                print("After Removing Element:", myset)
            except KeyError:
                print("Element not found in set!")
        elif choice == 5:
            myset.clear()
            print("Set Cleared.")
        elif choice == 6:
            print("Returning to Main Menu.")
            break
        else:
            print("Invalid choice... Please enter a number between 1 and 6...")


def dictoperations(mydict):
    while True:
        print("""\nDictionary Operations:
        1.About dictionaries
        2.Print Dictionary
        3.Access Value
        4.Add Key-Value Pair
        5.Remove Key
        6.Clear Dictionary
        7.Return to Main Menu""")

        choice = int(input("Enter your choice (1-7): "))
        if choice == 1:
            print('DEF: A Dictionary is a collection of key value pair of elements which is mutable and allows heterogenious type of data')
        elif choice == 2:
            print("Dictionary:", mydict)
        elif choice == 3:
            key_to_access = input("Enter a key to access from the dictionary: ")
            try:
                value = mydict[key_to_access]
                print("Value:", value)
            except KeyError:
                print("Key not found in dictionary!")
        elif choice == 4:
            new_key = input("Enter a new key to add to the dictionary: ")
            new_value = input("Enter the corresponding value: ")
            mydict[new_key] = new_value
            print("After Adding Key-Value Pair:", mydict)
        elif choice == 5:
            key_to_remove = input("Enter a key to remove from the dictionary: ")
            try:
                del mydict[key_to_remove]
                print("After Removing Key:", mydict)
            except KeyError:
                print("Key not found in dictionary!")
        elif choice == 6:
            mydict.clear()
            print("Dictionary Cleared.")
        elif choice == 7:
            print("Returning to Main Menu.")
            break
        else:
            print("Invalid choice... Please enter a number between 1 and 7...")
def stringoperations(mystring):
    while True:
        print("""\nString Operations:
        1.About Strings
        2.Print String
        3.Concatenate String
        4.Length of String
        5.Slice String
        6.String Repetition
        7.Uppercase and Lowercase
        8.Return to Main Menu""")

        choice = int(input("Enter your choice (1-8): "))
        if choice == 1:
            print('''DEF: A string is a collection of characters enclosed within single or double quotes. 
                  It is a primitive data structure in python \n ''')
        elif choice == 2:
            print("String:", mystring)
        elif choice == 3:
            another_string = input("Enter another string to concatenate: ")
            concatenated_string = mystring + " " + another_string
            print("Concatenated String:", concatenated_string)
        elif choice == 4:
            length_of_string = len(mystring)
            print("Length of String:", length_of_string)
        elif choice == 5:
            start_index = int(input("Enter the start index for slicing: "))
            end_index = int(input("Enter the end index for slicing: "))
            sliced_string = mystring[start_index:end_index]
            print("Sliced String:", sliced_string)
        elif choice == 6:
            repetition_factor = int(input("Enter the repetition factor: "))
            repeated_string = mystring * repetition_factor
            print("Repeated String:", repeated_string)
        elif choice == 7:
            uppercase_string = mystring.upper()
            lowercase_string = mystring.lower()
            print("Uppercase String:", uppercase_string)
            print("Lowercase String:", lowercase_string)
        elif choice == 8:
            print("Returning to Main Menu.")
            break
        else:
            print("Invalid choice. Please enter a number between 0 and 14.")

while True:
    print("""\nMain Menu:
    1. List Operations
    2. Tuple Operations
    3. Set Operations
    4. Dictionary Operations
    5. String Operations
    6. Exit""")

    choice = int(input("Enter your choice (1-6): "))

    if choice == 1:
        mylist = list(input("Enter values for List (space-separated): ").split())
        listoperations(mylist)
    elif choice ==2:
        mytuple = tuple(input("Enter values for Tuple (comma-separated): ").split(','))
        tupleoperations(mytuple)
    elif choice ==3:
        myset = set(input("Enter values for Set (space-separated): ").split())
        setoperations(myset)
    elif choice ==4:
        mydict= {}
        while True:
            key = input("Enter key for Dictionary (type 'exit' to stop): ")
            if key.lower() == 'exit':
                break
            value = input(f"Enter value for key '{key}': ")
            mydict[key]= value
        dictoperations(mydict)
    elif choice ==5:
        mystring = input("Enter a string :")
        stringoperations(mystring)
    elif choice ==6:
        print("Exiting the program... Goodbye!!")
        break
    else:
        print("Invalid choice... Please enter a number between 1 and 5...")
