# Task-1
import re

#Enter symbol
row=input("\nEnter words and numbers: ")

#Output of entered symbol
print("\nSymbol entered ", row)

extract_letter=" ".join(re.split("[0-9]+", row))
extract_number="".join(re.split("[a-zA-Z]+", row))
 
extract_com_let=", ".join(extract_letter.split())
extract_com_num=", ".join(extract_number.split())

#Derivation of numbers
print("\nAll numbers: ", str(extract_com_num))

#Derivation of words
print("\nAll words ", str(extract_com_let))


for let in extract_letter.split():
    print("\nDerivation of words with the first and last capital letters ", let[0].upper() + let[1:-1].lower() + let[-1].upper(), end="\n")

new_num_max=list(map(int, extract_number.split()))

max_num=max(new_num_max)

#Output the maximum value
print("\nMaximum value ", max_num)
for element in new_num_max:
    if element != max_num:
        element=element**new_num_max.index(element)
        print("\nThe numbers are elevated to the root of their index ", element)
    else:
        continue
