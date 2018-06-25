# Quiz03

#Dot Product

    def dot(vector01,vector02):
   
    """
    Inputs 2 vectors as arguments and returns the dot product of those vectors. This is done by first checking for the condition of the vectors being of equal dimensions. If the condition is met, the vectors are iterated through a for-loop so that each element in the list is multiplied by its respectively positioned element in the opposite vector. If the conditio is not met, the string 'invalid input' is returned.
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
      A function that perfroms vector subtraction by iterating through the elements within the vectors and iteratively subtracts the elements from one vector to the other. Finally, the resulting vector is stored in an empty list and printed.
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
    vector = [1,1]
    print(vecSubtract(vector01,vector02))


#Scalar Vector Multiplication

    def ScalarVecMulti(scalar,vector):
  
      """
      Function that inputs a vector aqnd a scalar and multiplies the values to return a new vector.
      This is done via a for-loop by stroing the new values inside premade empty values
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
      A function that iterates through each element in a list and determines the absolute value of the elements. By an if-statement, the code then finds the element with the greatest absolute value and returns that element's absolute value.
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
      A function that utilizes the previously defined infNorm function that iterates through the elements of a vector and using aritmetic with a scalar to form a normalized vector with respect to the norm. Once the values are created, the new elements are stored in an empty list using the .append function and finally the result is printed.
      """

      norm = infNorm(vector)  #calls value from previous function

      normed = [] #empty list for storing normalized vector

      for i in vector:  #iterates through the elements of the vector

        normed.append((1/norm)*i) #adds values of the vector to the empty list

      return normed

    vector = [1,2,3,4]
    vectorInv = [[1,4],[4,1]]
    print(normalize(vector))
