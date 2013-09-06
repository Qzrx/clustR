clustR
======

A terrible/naïve attempt at a zero-research clustering algorithm. That I came up with in the shower.

# clustR
#   A terrible, horrible, no-good, very bad clustering algorithm
# 
# Purpose:
#   I've thought about clustering/classification for a while; before I get into actually studying it I
#   wanted to try coming up with an algorithm for it myself--this is what I did for sorting, recommendation
#   systems, etc. and the result was a much faster assimilation of knowledge. So...here we go.
#
# How it works:
#   ClustR 'starts' in 2-dimensional space. I don't see any particular reason why it wouldn't be reduced
#   to 1 or N-dimensional. 2D is just kind of easy to start with mentally.
#   1) For each set of points, {x_a,y_a}, calculate the distances, D, between {x_1, y_1}, {x_2, y_2}, ..., {x_n, y_n}
#   2) For each D_{x_a, y_a}, calculate the minimum distance, D_m{x_a, y_a}
#   3) Calculate the mean minimum distance, M, as mean(D_m{x_1, y_1}, D_m{x_2, y_2}, ..., D_m{x_n, y_n})
#   4) Choose a starting point P at random a
#   5) Add P and all points within M distance of P to neighborhood N
#   5) Recurse 5) among all points now added to N
#   6) Recurse 4) for any point not yet in a neighborhood 

# Perils I need to watch out for:
#   IMPLEMENT THE DAMN ALGORITHM, NOT THE CODE
#   Don't hardcode things. Anything/everything should be a parameter--this includes how I'm calcualting distances
#     distance() should be a function. M should be a function. I can pass functions. USE THIS POWAH.
