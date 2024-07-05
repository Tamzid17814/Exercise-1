#Exercise 01: The list below is the collection of the ages of people from a
#village. Clean up the data and store only numbers in another list.
#data_list = [13, 24, 'Karim', {'name': 'guru'}, 45, 17]

data_list = [13, 24, 'Karim', {'name': 'guru'}, 45, 17]

numbers_list = []

for item in data_list:
    if isinstance(item, (int, float)):
        numbers_list.append(item)

print(numbers_list)


#Exercise 02: Find the most frequent character in the paragraph
#rhyme = 'Twinkle, twinkle, little star. How I wonder what you are!'


rhyme = 'Twinkle, twinkle, little star. How I wonder what you are!'.lower()
clean_up=rhyme.replace(' ','')
fre_char=max(clean_up,key=clean_up.count)
print(f"Most frequent{fre_char}")


#Exercise 03: Find the common items between the lists and make SUM of
#the new list items which are common between the lists.

list1 = [3, 5, 7, 4, 8, 8]
list2 = [4, 9, 8, 7, 1, 1, 13]

for i in list1:
    if i in list2:
        print(i)

#Exercise 04: Compare the two dictionaries and find the common items
#based on KEYs of the dictionaries
dict1 = {'age': 13, 'id': 12, 'address': 'Banani', 'course': 'Python'}
dict2 = {'address': 'Rupnagar', 'id': 25, 'course': 'MERN'}

for key in dict1:
    if key in dict2:
        print(key)



#Exercise 05: Sort the list in DESCENDING order and find the subtraction of
#maximum and minimum numbers.
list_12 = [4, 9, 8, 7, 5, 2, 13]
list_12.sort()
list_12.reverse()
max_num=max(list_12)
min_num=min(list_12)
print(list_12)
print(max_num+min_num)

#Exercise 06: Write conditional statements to identify the student’s average
#marks. If any subject’s mark is less than 40, you should print FAILED
#instead of making average marks
student_1 = [40, 35, 70, 90, 56]
student_2 = [57, 35, 80, 98, 46]


def calculate_average_marks(student):
    # Check if any mark is less than 40
    if any(mark < 40 for mark in student):
        print("FAILED")
    else:
        average_marks = sum(student) / len(student)
        print("Average marks:", average_marks)

print("Student 1:")
calculate_average_marks(student_1)

print("Student 2:")
calculate_average_marks(student_2)

