# Quiz03

#Dot Product

    def dot(vector01,vector02):
   
    """
    Takes 2 vectors and checks to see if they have the same dimension. If so, then the code iterates through the elements and returns the dot product of the vectors. If the vectors have different dimensions, then the string "Invalid Input" is returned and the vectors must be adjusted to fit the condition.
    """  
     
     element = 0 #empty value for storing data 
      
     if range(len(vector01)) == range(len(vector02)):  #condition that requires vectors to have same dimensions  
     
        for i in range(len(vector01)):  #iterates through rows of vector01      
        
          element += vector01[i]*vector02[i] #multiplies elements of each vector and adds products       
          
        return element      
        
      else: #condition for when dimensions are unequal
      
        return 'Invalid Input'
        
    #valid inputs
    vector01 = [1,2,0,4]
    vector02 = [1,1,10,1]
    #invalid inputs
    vector03 = [1,2,3]
    vector04 = [1,1]
    print(dot(vector01,vector02))


#Vector Subtraction

    def vecSubtract(vector01,vector02):
      """
      Takes 2 vectors and subtracts the elements from the first vector by the elements in the second and returns the new vector. For the vectors to be subtracted they must have the same dimension, if they don't match then the string "Invalid Input" is returned.
      """

      element = 0 #empty value for storing values of elements

      sub = []  #empty list for storing resulting vector

      if len(vector01) == len(vector02):  #condition that requires vectors to have same dimensions

        for i in range(len(vector01)):  ##iterates through rows of vector01

          element = vector01[i]-vector02[i] #stores values of individual elements

          sub.append(element) #creates new list from empty list

        return sub

      else:

        return "Invalid Input"

    #Valid Inputs
    vector01 = [1,2,3,4]
    vector02 = [10,11,21,1]
    #Invalid Inputs
    vector03 = [1,1,1,1]
    vector04 = [1,1]
    print(vecSubtract(vector01,vector02))


#Scalar Vector Multiplication

    def ScalarVecMulti(scalar,vector):
  
      """
      This function takes a vector and iterates through the elements to multiply each of the elements by a scalar to return the new vector.
      """

      element = 0 #empty value for storing elements of new vector

      product = []  #empty list for stoing new vector

      for i in range(len(vector)):  #iterates through rows of vector

        element = scalar*vector[i]  #stores new values from the proudct of the scalar and each element of the vector

        product.append(element) #adds values of vector to empty list

      return product

    scalar = -10
    vector = [1,20,-3]
    vectorInv = [[1,2],[3,4]]
    print(ScalarVecMulti(scalar,vector))


#Infinity Norm

    def infNorm(vector):
  
      """
      A function that iterates through each element in a list and determines the absolute value of the elements. Then, by the if-statement, the value of "norm" is replace by the greatest absolute value of each of the element.
      """

      norm = 0  #empty value for storing norm

      for i in vector:  #iterates through the rows of vector

        if norm < abs(i): #condition for finding absolute values of each element and giving element with greatest absolute value

          norm = abs(i) #gives the absolute value for each element

      return norm

    vector = [1,-15,14,-6,0]
    vectorInv = [[0,1],[11,2]]
    print(infNorm(vector))


#Normalized Vector

    def infNorm(vector):

      norm = 0

      for i in vector:

        if norm < abs(i):

         norm = abs(i)

      return norm

    def normalize(vector):

      """
     This code returns a vector that is normalized with respect to the previously defined infNorm value. The code does this by iterating through the elements and performs artihmetic and appends the new values to an empty list to create the desired vector.
      """

      norm = infNorm(vector)  #calls value from previous function

      normed = [] #empty list for storing normalized vector

      for i in vector:  #iterates through the elements of the vector

        normed.append((1/norm)*i) #adds values of the vector to the empty list

      return normed

    vector = [1,2,3,4]
    vectorInv = [[1,4],[4,1]]
    print(normalize(vector))
