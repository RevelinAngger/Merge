a1 = [1,4,6,7,8,10,11,12]
a2 = [-7,0,4,5,8,10,12,15]

def bruteForce(arr1,arr2):
    arr3 = []
    for i in range(len(arr1)):
        print(arr3)
        arr3.append(arr1[i])
    for i in range(len(arr2)):
        print(arr3)
        arr3.append(arr2[i])

    for i in range(1, len(arr3)): #insertion sort
        key = arr3[i]
        print(arr3)
        j = i-1
        while j >= 0 and key < arr3[j] :
                arr3[j + 1] = arr3[j]
                j -= 1
        arr3[j + 1] = key
    return arr3

def dynamicProgramming(arr1,arr2):
    arr3 = []
    i=0
    j=0
    
    while i<len(arr1) and j<len(arr1) :
        print(arr3)
        if arr1[i] < arr2[j]:
            arr3.append(arr1[i])
            i+=1
        else:
            arr3.append(arr2[j])
            j+=1
    
    while i<len(arr1):
        print(arr3)
        arr3.append(arr1[i])
        i+=1

    while j<len(arr2):
        print(arr3)
        arr3.append(arr2[j])
        j+=1

    return arr3

print(a1)
print(a2)
print(bruteForce(a1,a2))
print(dynamicProgramming(a1,a2))
