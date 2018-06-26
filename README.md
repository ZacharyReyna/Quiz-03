# Quiz-03

# Zachary Reyna
# R10381476
# Quiz 3

# extra work i was working on the side.
#vector01 = eval (input("Enter Vector Ex:(1,2,3): "))
#vector02 = eval (input("Enter second Vector:"))

# testing inputs 
vector01 = [1,2,4]
vector02 = [1,3,6]
vectorerror01 = [1,2,3]
vectorerror02 = [2,3,4,5]

def dot(vector01,vector02):
  '''
  Function dot(vector01, vector02) the user inputs the two Vectors he or she would like the DOT product form. first the function compares the two to make sure the number of elements are the same. Then use a for loop to muiltpy each element in each vector producing the DOT produce 
  '''
  a=len(vector01) # length of vector 1 for number of elements
  b=len(vector02)
  if a != b: # compare Vector length/ number of elements for vector1 & vector2 
    print('Error')
    return None

  ab=0 # empty set

  for i in range (a):
    ab += vector01[i] * vector02[i]  # math mult Vector1 and vector2 
  return ab # fills in the empty set ab

# Outputs 
print('The Dot product of vector01 and vector02 is ',dot(vector01,vector02))
#print(dot(vectorerror01,vectorerror02))
#####################################################

def vecSubtract(vector01,vector02):
  '''
  Function vecSubtract(vector01,vector02) the user inputs vector01 and vector02 where vector02 is subtracted from vector01. First the function compares the two Vector lengths, then uses a for loop to subtract each element then returns in the empty set cd.
  '''
  c=len(vector01) # length of vector01
  d=len(vector02)
  if c != d: # compares the number of elements in vector01 and vector02
    print('Error') # error if they do not match number of elements
    return None

  cd = [0] * c # empty set 

  for j in range (c): # in this for loop the math is computed
    cd[j] = vector02[j] - vector01[j]
  return cd # fills in the empty set

# Output 
print('The final vector from Subtracting Vector02 from Vector01 is',vecSubtract(vector01,vector02))
#print(vecSubtract(vectorerror01,vectorerror02))
#######################################################

# Inputs for Next three functions
scalar = 2
vector = [11,-5,-3]
scalarerror = [2,3]

def scalarVecMulti(scalar, vector):
  '''
  Function scalarVecMulti(scalar, vector) uses the Vector the user inputs to multiply by the scalar input. This function uses a For loop to multiply each element(k) in range of E which is the vector length/elements. Then returns the asnwer in the empty set ef.
  '''
  e=len(vector) # number of elements in vector fo the for loop 
  ef= [0] * e # creates empty set by the number of elements from vector 

  for k in range (e): # for loop where we multipy each vector element by the scalar input
    ef[k] = scalar * vector[k]

  return ef # fills in the empty set/ elements after solving

# Output 
print('The result of scalar Multiplied by Vector',scalarVecMulti(scalar, vector))
#print(scalarVecMulti(scalarerror, vectorerror01))
#####################################################


def infNorm(vector):
  '''
  The user provide an Vector input, with that input infNorm provides the Vector Norm which coverts the vector to absolute value then finds the max. first create an empty set , produce a for loop to compute each element. Then returns the value to gmax.
  '''
  g= len(vector)
  gh= [0] * g # empty set muli by num of str in the vector
  gmax=0

  for l in range (g): # set a range 
    gh[l] = abs(vector[l]) #abs vector
  for m in range (g): # finds the max in vector 
    if gmax < gh[m]:
      gmax = gh[m] 
  return gmax # fills in the empty set

# Outputs 
print('The inf Normal of Vector is',infNorm(vector)) # print answer
#print(infNorm(scalarerror)) 

######################################################


def normalize(vector):
  ''' 
  Function normalize(vector) which takes in a vector and returns the normalized vector with respect to the infinity norm. This function imports the answer from infNorm then uses a for loop to compute the answers from each element. also checks if the value is zero first.
  ''' 
  prev=infNorm(vector) # import answer from infNorm
  
  if prev == 0: # checks to see if the result is zero first
    return vector 

  r= len(vector) 
  finalvec = []  # empty set 
  for s in range(int(r)): # for loop to compute the answer 
   finalvec.append((1 / prev) * vector[s]) 
  return finalvec # returns value to the empty set.

# Outputs
print('The Normalized vector is',normalize(vector))
#print(normalize(scalar))
