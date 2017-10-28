.. qnum::
   :Prefix: 4-1-
   :start: 1
   
.. |start| image:: Figures/start.png
    :height: 24px
    :align: top
    :alt: start
    
.. |next| image:: Figures/next.png
    :height: 24px
    :align: top
    :alt: next
    
.. |Postv| image:: Figures/Prev.png
    :height: 24px
    :align: top
    :alt: Prev
    
.. |finish| image:: Figures/finishExam.png
    :height: 24px
    :align: top
    :alt: finishExam
    
.. |right| image:: Figures/rightArrow.png
    :height: 24px
    :align: top
    :alt: right arrow for next page
   
Posttest Multiple-Choice Questions
-----------------------------------

Please answer the following multiple-choice questions to the best of your ability.  Click the |start| button when you are ready to begin the exam.  Click on the |next| button below the question to display the next question.  Click on the |finish| button when you have answered all the questions that you can answer.   

.. timed:: Ex3Posttest2_mc
   :timelimit: 15
   :nofeedback:
   :retake:
       
   .. mchoice:: Ex3post2-1
      :answer_a: -3
      :answer_b: 4
      :answer_c: 5
      :answer_d: 7
      :answer_e: 10
      :correct: c
      :feedback_a: This answer would be true if the end value was 4 rather than 3.
      :feedback_b: This answer would be true if the start value was 0 rather than 1.
      :feedback_c: This would be true if it was looking for the largest value in the list from start to end (inclusive), but it finds the smallest value.
      :feedback_d: The range function returns a list from first to (last - 1) so this will look for the smallest value from index 1 to 3 and so return 3.  
      :feedback_e: This would be true if range returned a list of values from the first to last but it returns from first to last - 1.

      What does the following function return from function1([4, 7, 10, 5, -3],1,3)?
       
      ::
          
           def function1(nums, first, last):
               temp = nums[first]
               for index in range(first,last+1):
                  current = nums[index]
                  if current < temp:
                      temp = current
               return temp
               
   .. mchoice:: Ex3post2-2
      :answer_a: 4
      :answer_b: 3
      :answer_c: 2
      :answer_d: 1
      :answer_e: 0
      :correct: c
      :feedback_a: Wrong
      :feedback_b: Wrong
      :feedback_c: Right
      :feedback_d: Wrong
      :feedback_e: Wrong

      Consider the following code fragment.  What will it print when it executes?
      ::
               
           nums1 = [2, 3, 4, 6]
           nums2 = [2, 3, 5, 6]
           i1 = len(nums1) - 1
           i2 = len(nums2) - 1
           count = 0
           while i1 > 0 and i2 > 0:
               if nums1[i1] == nums2[i2]:
                   count=count + 1
                   i1 = i1 - 1
                   i2 = i2 - 1
               elif nums1[i1] < nums2[i2]:
                   i2 = i2 - 1
               else:
                   i1 = i1 - 1
           print(count)    
               
          
   .. mchoice:: Ex3post2-3
      :answer_a: 0
      :answer_b: 1
      :answer_c: 2
      :answer_d: 3
      :answer_e: 4
      :correct: a
      :feedback_a: While this loops through the indices from 1 to 3 it compares the index to the target and so count remains 0.
      :feedback_b: This would be true if it compared the value at the index to the target, but it compares the index to the target.
      :feedback_c: This would be true if the range included the last value and the code compared the value at the index to the target.
      :feedback_d: This would be true if the start value was 0 and the range included the last value, and the code compared the value at the index to the target.
      :feedback_e: This would be true if the start value was 0 and the end value was 6 and the code compared the value at the index to the target. 

      Given the following function definition, what would be returned from function2(7, 1, 4, [7, 3, 7, 7, 7])?
      ::

          def function2(value, first, last, nums):
              total = 0
              for index in range(first, last):
                  next = index
                  if next == value:
                      total = total + 1
              return total
          
   .. mchoice:: Ex3post2-4
      :answer_a: x = 8 and y = 0
      :answer_b: x = 9 and y = -1
      :answer_c: x = 2 and y = 6
      :answer_d: x = 5 and y = 3
      :answer_e: x = 3 and y = 5
      :correct: e
      :feedback_a: This would be true if it was range(1,3).
      :feedback_b: This would be true if it was range(1,5).  Remember that range doesn't include the second value.
      :feedback_c: Not quite.  Check your tracing.
      :feedback_d: Not quite.  Check your tracing.  
      :feedback_e: Good job tracing this! 

      What do ``x`` and ``y`` equal after the following code executes?
      ::

          x = 7
          y = 1
          z = 0
          for i in range(1,4):
              z = x
              x = i + y
              y = z - i
              
   .. mchoice:: Ex3post2-5
      :answer_a: 25.0
      :answer_b: 40.0
      :answer_c: 45.0
      :answer_d: 35.0
      :answer_e: 0
      :correct: d
      :feedback_a: This would be true if start was 0 and end was 1.
      :feedback_b: This would be true if start was 2 and end was 2.
      :feedback_c: This would be true if start was 0 and end was 2.  
      :feedback_d: This is 30 + 40 = 70 / 2 = 35.0.
      :feedback_e: This would be true if end was less than start.  

      Given the following code what will function3([20,30,40],1,2) return?
      ::
      
          def function3(nums, first, last):
              total = 0
              for index in range(first,last+1):
                  current = nums[index]
                  total = total + current
              if (last - first + 1) >= 1:
                  return total / (last - first + 1)
              return 0
              
		   
           
          
   
		   
When you are finished answering all the questions you can, click the |finish| button and then go to the next page by clicking the right arrow |right| near the bottom right of this page.   