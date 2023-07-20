# Leetcode 735. Asteroid Collision (Medium)

# Problem

We are given an array asteroids of integers representing asteroids in a row.

For each asteroid, the absolute value represents its size, and the sign represents its direction (positive meaning right, negative meaning left). Each asteroid moves at the same speed.

Find out the state of the asteroids after all collisions. If two asteroids meet, the smaller one will explode. If both are the same size, both will explode. Two asteroids moving in the same direction will never meet.

# Solution O(N)

Starting at the left of the the array, pass over negative asteroids until you find a positive asteroid, from there continue right until the next asteroid is a negative one. Then check which or both of the asteroids will be destroyed. If the negative(right) asteroid is destroyed, pop it from the array. If the positive(left) asteroid is destroyed, pop it from the array and reduce i by one, continue. Once you reach the end of the array return the array.
