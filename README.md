# Working-on-an-Image
### Aim:
 To divide two images into quadrants, swap specific regions between them, and resize the final images according to specified dimensions.
###  Software Required:
Anaconda - Python 3.7
### Algorithm:
1. **Load Images**: Load two images of the same size.
2. **Divide into Quadrants**: Split each image into four equal region using row and column coordinates.
3. **Swap Regions**: Swap regions as follows: R1 with R8 and R2 with R7.
4. **Merge Quadrants**: Reassemble the images with the swapped quadrants.
5. **Resize**: Resize the final images to match the dimensions.
### Program:
```
Developed By:KARTHIKEYAN R
Register Number:212222240046
```
```
import cv2
image1= cv2.imread('pic.jpg')
image2= cv2.imread('pic1.jpg')
image1_resized = cv2.resize(image1,(400,400))
image2_resized = cv2.resize(image2,(400,400))
R1 = image1_resized [0:200, 0:200] #Top-Left region
R2 = image1_resized [0:200, 200:400] # Top-right region
R3 =image1_resized [200:400, 0:200] # Bottom-left region
R4 = image1_resized [200:400, 200:400] # Bottom-right 
R5 = image2_resized [0:200, 0:200]
R6= image2_resized [0:200, 200:400] # Top-right region
R7= image2_resized [200:400, 0:200] # Bottom-left region
R8 =image2_resized [200:400, 200:400] 
image1_resized [0:200, 0:200] = R8 
image2_resized [200:400, 200:400] =R3
cv2.imshow("Image1", image1_resized)
cv2.imshow("Image2", image2_resized)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:
![](https://github.com/user-attachments/assets/5b0aaf10-c4da-4e21-9c5b-0229041103a8)
![](https://github.com/user-attachments/assets/a8d01aed-896b-4c22-904d-c42f8d5375ca)


### Result:
Two images were successfully divided into quadrants, specific regions swapped, and resized to the specified dimensions.
