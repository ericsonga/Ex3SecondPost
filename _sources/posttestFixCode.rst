.. qnum::
   :Prefix: 4-2-
   :start: 1

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button
   
.. |pass| image:: Figures/pass.png
    :height: 20px
    :align: top
    :alt: pass
    
.. |fail| image:: Figures/fail.png
    :height: 20px
    :align: top
    :alt: fail
    
.. |checkme| image:: Figures/checkMe.png
    :height: 20px
    :align: top
    :alt: check me
    
.. |start| image:: Figures/start.png
    :height: 24px
    :align: top
    :alt: start
    
.. |finish| image:: Figures/finishExam.png
    :height: 24px
    :align: top
    :alt: finishExam
    
.. |right| image:: Figures/rightArrow.png
    :height: 24px
    :align: top
    :alt: right arrow for next page

               
Posttest Fix Code Problem
----------------------------
    
The code below is trying to calculate the average, but also doubles the largest value in the list, but it contains errors. If there are no items in the list it should return 0.

Examples
=========

For example, ``getAverageDoubleLargest([1,1,3])`` should return 2 since the total of all the values in the list is (1 + 1 + 3) = 5.  Adding the largest value, 3, again to the total is (5 + 3) = 8.  Dividing by the number of items in the list plus one is (8 / (3 + 1 = 4) = 2). 
While ``getAverageDoubleLargest([-3.0,-3.0,-5.0])`` should return -3.5 since the total of all the values in the list is (-11.0).  Adding the largest value, -3, again to the total is (-11.0 + -3.0 = -14.0).  Dividing by the number of items in the list plus one is (-14 / (3 + 1 = 4) = -3.5. 

Fix Code Here
==============

Fix the errors so that the hidden tests all print |pass| when you click the |runbutton| button. The error messages and test results are displayed below the code. 
               
Click on the |start| button below when you are ready to try to fix this code.  You will have up to 10 minutes to try to solve it.  Click on the |runbutton| button to run and test the code.  Click on the |finish| button when you have solved this problem or wish to move on without solving it.

.. timed:: Posttest2_Average_double_largest
   :timelimit: 10
   :noresult:
   :nofeedback:
   :fullwidth:
    
   .. activecode:: Posttest2_Average_Double_Largest
   
      def getAverageDoubleLargest(values):
          
          #if no value in list return 0
          if len(values) = 0:
              return 0

          # initialize variables
          total = 0
          largest = 0
          
          # loop through indicies
          for index in range(values):
          
              # get value and add to total
              value = values[index]
              total = total + value
              
          # check for new largest
          if value < largest:
              largest = value
              
          # return average with doubled largest
          total = total + largest
          return total / len(values)
          
      ====
          
      # code to test the getAverageDoublelargest function        
      from unittest.gui import TestCaseGui
      
      class myTests(TestCaseGui):

          def testTarget(self):
              self.assertEqual(getAverageDoubleLargest([1,1,3]), 2, "Test of getAverageDoubleLargest([1,1,3])")
              self.assertEqual(getAverageDoubleLargest([]),0, "Test of getAverageDoubleLargest([])")
              self.assertEqual(getAverageDoubleLargest([3.0,5.0,2.0,0]), 3.0, "Test of getAverageDoubleLargest([3.0,5.0,2.0,0]")
              self.assertEqual(getAverageDoubleLargest([-3.0,-3.0,-5.0]),-3.5, "Test of getAverageDoubleLargest([-3,-3,-5]")
              
		   
      myTests().main()

When you are finished with this problem, or are ready to move on, click the |finish| button and then go to the next page by clicking the right arrow |right| near the bottom right of this page.    
