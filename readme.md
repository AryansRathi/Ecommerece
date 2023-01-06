**Computer Vision[**](#Computer-Vision)**

**Jacobs University Bremen[**](#Jacobs-University-Bremen)**

**Fall 2022[**](#Fall-2022)**

**Homework 2[**](#Homework-2)**

*This notebook includes both coding and written questions. Please hand in this notebook file with all the outputs and your answers to the written questions.*

This assignment covers linear filters, convolution and correlation.

In [1]:

*# Setup*

**import** **numpy** **as** **np**

**import** **matplotlib.pyplot** **as** **plt**

**from** **time** **import** time

**from** **skimage** **import** io

**from** **\_\_future\_\_** **import** print\_function

%matplotlib inline

plt.rcParams['figure.figsize'] = (10.0, 8.0) *# set default size of plots*

plt.rcParams['image.interpolation'] = 'nearest'

plt.rcParams['image.cmap'] = 'gray'

*# for auto-reloading extenrnal modules*

%load\_ext autoreload

%autoreload 2

**Part 1: Convolutions[**](#Part-1:-Convolutions)**

**1.1 Commutative Property (10 points)[**](#1.1-Commutative-Property-\(10-points\))**

Recall that the convolution of an image $f:\mathbb{R}^2\rightarrow \mathbb{R}$ and a kernel $h:\mathbb{R}^2\rightarrow\mathbb{R}$ is defined as follows: $$(f\*h)[m,n]=\sum\_{i=-\infty}^\infty\sum\_{j=-\infty}^\infty f[i,j]\cdot h[m-i,n-j]$$

Or equivalently, \begin{align} (f\*h)[m,n] &= \sum\_{i=-\infty}^\infty\sum\_{j=-\infty}^\infty h[i,j]\cdot f[m-i,n-j]\\ &= (h\*f)[m,n] \end{align}

Show that this is true (i.e. prove that the convolution operator is commutative: $f\*h = h\*f$).

**Your Answer:** *Write your solution in this markdown cell. Please write your equations in [LaTex equations](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Typesetting%20Equations.html).* $$ (f\*h)[m.n] =\sum\_{i = -\infty}^{\infty} \sum\_{j = -\infty}^{\infty} f[i,j] . h[m-i,n-j] = \int\_{-\infty}^{\infty} \int\_{-\infty}^{\infty} f[i,j] . h[m-i,n-j] \ di \ dj $$

Let,

$$ m-i = x \rightarrow i=m-x \rightarrow \frac{d}{dx}i = \frac{d}{dx}(m-x) \rightarrow \frac{d}{dx}i=-1 \rightarrow di=-dx $$$$ n-j = y \rightarrow j=n-y \rightarrow \frac{d}{dy}j = \frac{d}{dy}(n-y) \rightarrow \frac{d}{dy}j=-1 \rightarrow dj=-dy $$

From $x=m-i$, when $ i\rightarrow \infty, x\rightarrow -\infty $ and when $ i \rightarrow -\infty, x\rightarrow \infty $

From $y=n-j$, when $ j\rightarrow \infty, y\rightarrow -\infty $ and when $ j \rightarrow -\infty, y\rightarrow \infty $

Replacing the values in initial equation,

$$ (f\*h)[m.n] = \int\_{\infty}^{-\infty} \int\_{\infty}^{-\infty} f[m-x,n-y] . h[x,y] \ dx \ dy $$

Flipping the integrals,

$$ (f\*h)[m.n] = -1 \times -1 \times \int\_{-\infty}^{\infty} \int\_{-\infty}^{\infty} h[x,y] . f[m-x,n-y] \ dx \ dy $$$$ (f\*h)[m.n] = \int\_{-\infty}^{\infty} \int\_{-\infty}^{\infty} h[x,y] . f[m-x,n-y] \ dx \ dy $$$$ (f\*h)[m.n] = (h\*f)[m.n] $$

$\therefore$ Proved.

**1.2 Implementation (30 points)[**](#1.2-Implementation-\(30-points\))**

In this section, you will implement two versions of convolution:

- conv\_nested
- conv\_fast

First, run the code cell below to load the image to work with.

In [2]:

*# Open image as grayscale*

img = io.imread('dog.jpg',as\_gray=**True**) 

*# Show image*

plt.imshow(img)

plt.axis('off')

plt.title("Isn't he cute?")

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.001.png)

Now, implement the function **conv\_nested** in **filters.py**. This is a naive implementation of convolution which uses 4 nested for-loops. It takes an image $f$ and a kernel $h$ as inputs and outputs the convolved image $(f\*h)$ that has the same shape as the input image. This implementation should take a few seconds to run.

*- Hint: It may be easier to implement $(h*f)$\*

We'll first test your conv\_nested function on a simple input.

In [3]:

**from** **filters** **import** conv\_nested

*# Simple convolution kernel.*

kernel = np.array(

[

`    `[1,0,1],

`    `[0,0,0],

`    `[1,0,0]

])

*# Create a test image: a white square in the middle*

test\_img = np.zeros((9, 9))

test\_img[3:6, 3:6] = 1

*# Run your conv\_nested function on the test image*

test\_output = conv\_nested(test\_img, kernel)

*# Build the expected output*

expected\_output = np.zeros((9, 9))

expected\_output[2:7, 2:7] = 1

expected\_output[5:, 5:] = 0

expected\_output[4, 2:5] = 2

expected\_output[2:5, 4] = 2

expected\_output[4, 4] = 3

*# Plot the test image*

plt.subplot(1,3,1)

plt.imshow(test\_img)

plt.title('Test image')

plt.axis('off')

*# Plot your convolved image*

plt.subplot(1,3,2)

plt.imshow(test\_output)

plt.title('Convolution')

plt.axis('off')

*# Plot the exepected output*

plt.subplot(1,3,3)

plt.imshow(expected\_output)

plt.title('Exepected output')

plt.axis('off')

plt.show()

*# Test if the output matches expected output*

**assert** np.max(test\_output - expected\_output) < 1e-10, "Your solution is not correct."

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.002.png)

Now let's test your conv\_nested function on a real image.

In [4]:

**from** **filters** **import** conv\_nested

*# Simple convolution kernel.*

*# Feel free to change the kernel to see different outputs.*

kernel = np.array(

[

`    `[1,0,-1],

`    `[2,0,-2],

`    `[1,0,-1]

])

out = conv\_nested(img, kernel)

*# Plot original image*

plt.subplot(2,2,1)

plt.imshow(img)

plt.title('Original')

plt.axis('off')

*# Plot your convolved image*

plt.subplot(2,2,3)

plt.imshow(out)

plt.title('Convolution')

plt.axis('off')

*# Plot what you should get*

solution\_img= io.imread('convoluted\_dog.jpg',as\_gray=**True**)

plt.subplot(2,2,4)

plt.imshow(solution\_img)

plt.title('What you should get')

plt.axis('off')


plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.003.png)

Let us implement a more efficient version of convolution using array operations in numpy. As shown in the lecture, a convolution can be considered as a sliding window that computes sum of the pixel values weighted by the flipped kernel. The faster version will i) zero-pad an image, ii) flip the kernel horizontally and vertically, and iii) compute weighted sum of the neighborhood at each pixel.

First, implement the function **zero\_pad** in **filters.py**.

In [5]:

**from** **filters** **import** zero\_pad

pad\_width = 20 *# width of the padding on the left and right*

pad\_height = 40 *# height of the padding on the top and bottom*

padded\_img = zero\_pad(img,pad\_height,pad\_width)

*# Plot your padded dog*

plt.subplot(1,2,1)

plt.imshow(padded\_img)

plt.title('Padded dog')

plt.axis('off')

*# Plot what you should get*

solution\_img = io.imread('convoluted\_dog.jpg',as\_gray=**True**)

plt.subplot(1,2,2)

plt.imshow(solution\_img)

plt.title('What you should get')

plt.axis('off')

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.004.png)

Next, complete the function **conv\_fast** in **filters.py** using zero\_pad. Run the code below to compare the outputs by the two implementations. conv\_fast should run significantly faster than conv\_nested.
Depending on your implementation and computer, conv\_nested should take a few seconds and conv\_fast should be around 5 times faster.

In [6]:

**from** **filters** **import** conv\_fast

t0 = time()

out\_fast = conv\_fast(img, kernel)

t1 = time()

out\_nested = conv\_nested(img, kernel)

t2 = time()

*# Compare the running time of the two implementations*

print("conv\_nested: took **%f** seconds." % (t2 - t1))

print("conv\_fast: took **%f** seconds." % (t1 - t0))

*# Plot conv\_nested output*

plt.subplot(1,2,1)

plt.imshow(out\_nested)

plt.title('conv\_nested')

plt.axis('off')

*# Plot conv\_fast output*

plt.subplot(1,2,2)

plt.imshow(out\_fast)

plt.title('conv\_fast')

plt.axis('off')

*# Make sure that the two outputs are the same*

**if** **not** (np.max(out\_fast - out\_nested) < 1e-10):

`    `print("Different outputs! Check your implementation.")

conv\_nested: took 0.533825 seconds.

conv\_fast: took 0.360928 seconds.

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.005.png)

-----
**Part 2: Cross-correlation[**](#Part-2:-Cross-correlation)**

Cross-correlation of two 2D signals $f$ and $g$ is defined as follows: $$(f\star{g})[m,n]=\sum\_{i=-\infty}^\infty\sum\_{j=-\infty}^\infty f[i,j]\cdot g[i-m,j-n]$$

**2.1 Template Matching with Cross-correlation (12 points)[**](#2.1-Template-Matching-with-Cross-correlation-\(12-points\))**

Suppose that you are a clerk at a grocery store. One of your responsibilites is to check the shelves periodically and stock them up whenever there are sold-out items. You got tired of this laborious task and decided to build a computer vision system that keeps track of the items on the shelf.

Luckily, you have learned in the Computer Vision class at Jacobs University that cross-correlation can be used for template matching: a template $g$ is multiplied with regions of a larger image $f$ to measure how similar each region is to the template.

The template of a product (template.jpg) and the image of shelf (shelf.jpg) is provided. We will use cross-correlation to find the product in the shelf.

Implement **cross\_correlation** function in **filters.py** and run the code below.

*- Hint: you may use the conv\_fast function you implemented in the previous question.*

In [7]:

**from** **filters** **import** cross\_correlation

*# Load template and image in grayscale*

img = io.imread('shelf.jpg')

img\_grey=io.imread('shelf.jpg',as\_gray=**True**)

temp = io.imread('template.jpg')

temp\_grey=io.imread('template.jpg',as\_gray=**True**)

*# Perform cross-correlation between the image and the template*

out = cross\_correlation(img\_grey, temp\_grey)

*# Find the location with maximum similarity*

y,x = (np.unravel\_index(out.argmax(), out.shape))

*# Display product template*

plt.figure(figsize=(25,20))

plt.subplot(3, 1, 1)

plt.imshow(temp)

plt.title('Template')

plt.axis('off')

*# Display cross-correlation output*

plt.subplot(3, 1, 2)

plt.imshow(out)

plt.title('Cross-correlation (white means more correlated)')

plt.axis('off')

*# Display image*

plt.subplot(3, 1, 3)

plt.imshow(img)

plt.title('Result (blue marker on the detected location)')

plt.axis('off')

*# Draw marker at detected location*

plt.plot(x, y, 'bx', ms=40, mew=10)

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.006.png)

**Interpretation[**](#Interpretation)**

How does the output of cross-correlation filter look? Was it able to detect the product correctly? Explain what problems there might be with using a raw template as a filter.

**Your Answer:** *Write your solution in this markdown cell.* The ouput is not correct as the filter is not able to detect the product that we are searching. This is beacause the raw template does not have zero mean value.

-----
**2.2 Zero-mean cross-correlation (6 points)[**](#2.2-Zero-mean-cross-correlation-\(6-points\))**

A solution to this problem is to subtract the mean value of the template so that it has zero mean.

Implement **zero\_mean\_cross\_correlation** function in **filters.py** and run the code below.

In [9]:

**from** **filters** **import** zero\_mean\_cross\_correlation

*# Perform cross-correlation between the image and the template*

out = zero\_mean\_cross\_correlation(img\_grey, temp\_grey)

*# Find the location with maximum similarity*

y,x = (np.unravel\_index(out.argmax(), out.shape))

*# Display product template*

plt.figure(figsize=(30,20))

plt.subplot(3, 1, 1)

plt.imshow(temp)

plt.title('Template')

plt.axis('off')

*# Display cross-correlation output*

plt.subplot(3, 1, 2)

plt.imshow(out)

plt.title('Cross-correlation (white means more correlated)')

plt.axis('off')

*# Display image*

plt.subplot(3, 1, 3)

plt.imshow(img)

plt.title('Result (blue marker on the detected location)')

plt.axis('off')

*# Draw marker at detcted location*

plt.plot(x, y, 'bx', ms=40, mew=10)

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.007.png)

You can also determine whether the product is present with appropriate scaling and thresholding.

In [13]:

**def** check\_product\_on\_shelf(shelf, product):

`    `out = zero\_mean\_cross\_correlation(shelf, product)



`    `*# Scale output by the size of the template*

`    `out = out / float(product.shape[0]\*product.shape[1])



`    `*# Threshold output (this is arbitrary, you would need to tune the threshold for a real application)*

`    `out = out > 0.025



`    `**if** np.sum(out) > 0:

`        `print('The product is on the shelf')

`    `**else**:

`        `print('The product is not on the shelf')

*# Load image of the shelf without the product*

img2= io.imread('shelf.jpg')

img2\_grey=io.imread('shelf\_soldout.jpg',as\_gray=**True**)


plt.imshow(img)

plt.axis('off')

plt.show()

check\_product\_on\_shelf(img\_grey, temp\_grey)

plt.imshow(img2)

plt.axis('off')

plt.show()

check\_product\_on\_shelf(img2\_grey, temp\_grey)

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.008.png)

The product is on the shelf

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.008.png)

The product is not on the shelf

-----
**2.3 Normalized Cross-correlation (12 points)[**](#2.3-Normalized-Cross-correlation-\(12-points\))**

One day the light near the shelf goes out and the product tracker starts to malfunction. The zero\_mean\_cross\_correlation is not robust to change in lighting condition. The code below demonstrates this.

In [13]:

**from** **filters** **import** normalized\_cross\_correlation

*# Load image*

img = io.imread('shelf\_dark.jpg')

img\_grey=io.imread('shelf\_soldout.jpg',as\_gray=**True**)

*# Perform cross-correlation between the image and the template*

out = zero\_mean\_cross\_correlation(img\_grey, temp\_grey)

*# Find the location with maximum similarity*

y,x = (np.unravel\_index(out.argmax(), out.shape))

*# Display image*

plt.imshow(img)

plt.title('Result (red marker on the detected location)')

plt.axis('off')

*# Draw marker at detcted location*

plt.plot(x, y, 'rx', ms=25, mew=5)

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.009.png)

A solution is to normalize the pixels of the image and template at every step before comparing them. This is called **normalized cross-correlation**.

The mathematical definition for normalized cross-correlation of $f$ and template $g$ is: $$(f\star{g})[m,n]=\sum\_{i,j} \frac{f[i,j]-\overline{f\_{m,n}}}{\sigma\_{f\_{m,n}}} \cdot \frac{g[i-m,j-n]-\overline{g}}{\sigma\_g}$$

where:

- $f\_{m,n}$ is the patch image at position $(m,n)$
- $\overline{f\_{m,n}}$ is the mean of the patch image $f\_{m,n}$
- $\sigma\_{f\_{m,n}}$ is the standard deviation of the patch image $f\_{m,n}$ 
- $\overline{g}$ is the mean of the template $g$
- $\sigma\_g$ is the standard deviation of the template $g$

Implement **normalized\_cross\_correlation** function in **filters.py** and run the code below.

In [14]:

**from** **filters** **import** normalized\_cross\_correlation

*# Perform normalized cross-correlation between the image and the template*

out = normalized\_cross\_correlation(img\_grey, temp\_grey)

*# Find the location with maximum similarity*

y,x = (np.unravel\_index(out.argmax(), out.shape))

*# Display image*

plt.imshow(img)

plt.title('Result (red marker on the detected location)')

plt.axis('off')

*# Draw marker at detcted location*

plt.plot(x, y, 'rx', ms=25, mew=5)

plt.show()

![](Aspose.Words.4528ee4e-8f05-4842-abfe-1ed10e971693.010.png)

**Part 3: Separable Filters[**](#Part-3:-Separable-Filters)**

**3.1 Theory (10 points)[**](#3.1-Theory-\(10-points\))**

Consider an $M\_1\times{N\_1}$ image $I$ and an $M\_2\times{N\_2}$ filter $F$. A filter $F$ is **separable** if it can be written as a product of two 1D filters: $F=F\_1F\_2$.

For example, $$F= \begin{bmatrix} 1 & -1 \\ 1 & -1 \end{bmatrix} $$ can be written as a matrix product of $$F\_1= \begin{bmatrix} 1 \\ 1 \end{bmatrix}, F\_2= \begin{bmatrix} 1 & -1 \end{bmatrix} $$ Therefore $F$ is a separable filter.

Prove that for any separable filter $F=F\_1F\_2$, $$I\*F=(I\*F\_1)\*F\_2$$

**Your Answer:** *Write your solution in this markdown cell. Please write your equations in [LaTex equations](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Typesetting%20Equations.html).* iven, we have three filters $F, F\_1, F\_2,$ and an identity matrix $I$.

To Prove: For any seperable filter $F = F\_1 F\_2$, $I\*F = (I\*F\_1) \* F\_2$

Proof: We know that any matrix, say $A$, multiplied by an identity matrix gives the original matrix $A$. $$ LHS = I \* F = F = F\_1 F\_2 $$ $$ RHS = (I\*F\_1) \* F\_2 = F\_1 F\_2 $$ $\therefore LHS = RHS $

$\therefore$ For any separable filter $F = F\_1 F\_2$, $I\*F = (I\*F\_1) \* F\_2$

$\therefore$ Proved.
