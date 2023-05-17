# Programming_Assingment-14



1. Define a class with a generator which can iterate the numbers, which are divisible by 7, between a given range 0 and n.
sol:
class Task1:
    def gen(self, n):
        for i in range(n+1):
            if i%7 == 0:
                yield i
nums = Task1()
[i for i in nums.gen(100)]
[0, 7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98]



2. Write a program to compute the frequency of the words from the input. The output should output after sorting the key alphanumerically.
sol:
def task2(string: str):
    
    string_list = string.split(' ')
    out_dict = {}
    
    for s in string_list:
        if s in out_dict.keys():
            out_dict[s] += 1
        else:
            out_dict[s] = 1
            
    for k, v in sorted(out_dict.items()):
        print(k, ':', v)
task2('New to Python or choosing between Python 2 and Python 3? Read Python 2 or Python 3')
2 : 2
3 : 1
3? : 1
New : 1
Python : 5
Read : 1
and : 1
between : 1
choosing : 1
or : 2
to : 1



3. Define a class Person and its two child classes: Male and Female. All classes have a method "getGender" which can print "Male" for Male class and "Female" for Female class.
sol:
class Person:
    def getGender(self):
        pass
    
class Male(Person):
    def getGender(self):
        print('Male')
        
class Female(Person):
    def getGender(self):
        print('Female')
male = Male()
female= Female()
male.getGender()
female.getGender()
Male
Female




4. Please write a program to generate all sentences where subject is in ["I", "You"] and verb is in ['Play', "Love"] and the object is in ["Hockey","Football"].
sol:
subject=["I", "You"]
verb=["Play", "Love"]
obj=["Hockey","Football"]

sentence_list = []

for i in subject:
    for j in verb:
        for k in obj:
            sentence_list.append(i + " " + j + " " + k)
            
for sentence in sentence_list:
    print(sentence)
I Play Hockey
I Play Football
I Love Hockey
I Love Football
You Play Hockey
You Play Football
You Love Hockey
You Love Football




5. Please write a program to compress and decompress the string "hello world!hello world!hello world!hello world!"
sol:
import zlib

string = 'hello world!hello world!hello world!hello world!'

compress_string = zlib.compress(bytes(s, 'utf-8'))

print(f"Compressed string is: {compress_string}")
print(f"Decompressed string is: {zlib.decompress(compress_string)}")
Compressed string is: b'x\x9c\xcbH\xcd\xc9\xc9W(\xcf/\xcaIQ\xcc \x82\r\x00\xbd[\x11\xf5'
Decompressed string is: b'hello world!hello world!hello world!hello world!'




6. Please write a binary search function which searches an item in a sorted list. The function should return the index of element to be searched in the list.
sol:
def binarySearch(list1, n):  
    
    
    low = 0  
    high = len(list1) - 1  
    mid = 0  
  
    while low <= high:  
        mid = (high + low) // 2  
        if list1[mid] < n:  
            low = mid + 1  
        elif list1[mid] > n:  
            high = mid - 1  
        else:  
            return mid  
    return -1
sorted_list = [1, 4, 5, 12, 54, 678, 1235]

binarySearch(sorted_list, 54)
4




