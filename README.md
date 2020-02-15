# Barycenter2D
Calculates the barycenter of an intensity image

The calculation of barycenter indices of a heatmap intensity information (C, in Matlab imagesc) is based on the following forum answers:
(1) https://www.mathworks.com/matlabcentral/answers/133395-compute-centroid-of-a-matrix
(2) https://www.mathworks.com/matlabcentral/answers/363181-center-of-mass-and-total-mass-of-a-matrix
To convert the index information to coordinates, a linear fit between the original coordinate vectors x, y and the index vectors xIdx, yIdx is performed analytically to get the slopes and intercepts for both fits (Note: you could also use the function p = polyval(x,y,1) to calculate slope (p(1)) and intercept (p(2)) as well). The calculated indices for barycenterIdxX and barycenterIdxY of either method (1) or method (2) are used to evaluate the linear fit to get the barycenter coordinate values (barycenterX, barycenterY; assuming that x and y are evenly spaced), which, for example, can be plotteded onto the image.

Test data on plot are included and must be un-commented at the beginning and end of the function, respectively.
