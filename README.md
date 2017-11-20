# EightQueen

## Problem
Eight Queens is a classical problem where the idea is to place eight queens on a chess board such that no two attack eachother. Queens in chess are allowed to move ('attack') horizontally, vertically and diagonally.

## Algorithm
The eight queen problem will be posed as a Constraint Satisfaction Problem (CSP). A CSP has to satisfy a set of constraints at every state. The algorithm used is Minimum Conflicts method of CSP.

~~~
  '''
  algorithm''' MIN-CONFLICTS
      '''input:''' ''csp'', a constraint satisfaction problem
             ''max_steps'',the number of steps allowed before giving up
             ''current_state'', an initial assignment of values for the variables in the csp
      '''output:''' a solution set of values for the variable '''or''' ''failure''
    '''for''' i=1 to max_steps '''do'''
        '''if''' ''current_state'' is a solution of ''csp'' '''then''' return ''current_state''
        ''var'' <-- a randomly chosen variable from the set of conflicted variables CONFLICTED[''csp'']
        ''value'' <-- the value v for ''var'' that minimizes CONFLICTS(''var'',''v'',''current_state'',''csp'')
        '''set''' ''var'' = ''value'' in ''current_state''
    '''return''' ''failure''
~~~
