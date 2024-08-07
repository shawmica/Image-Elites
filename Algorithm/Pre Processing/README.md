Image pre-processing phase


In the pre-processing phase. 1st we loaded sample images of all the 14 days and here we showed the sample 20th image which is from pixel device throughout this algorithm process.

![image](https://github.com/user-attachments/assets/65aaf098-0e2f-4bc2-9f08-8867669d34fd)
20th image
 

After loaded sample images we cropped white background for avoid the unnecessary influence in our calculation
![image](https://github.com/user-attachments/assets/9fb9c295-c707-4b3f-a7a5-1795a3ad9c18)---> ![image](https://github.com/user-attachments/assets/dea578df-6bd7-4d4c-a708-fe7c5be7bc36)






In order to apply gaussian blur to make this process efficient and to simplify the cropped samples by reducing 3 channels into 1 channel. After that we applied gaussian blur to reduce random noise which were produced during dataset preparation. In this stage you may think why we didn't choose other filters? After the noise reduction process we need to sharpen the images. For sharpening we choose to apply laplacian filter. To make this sharpened image more effective we decided that gaussian blur is the best choice.








Next, we applied laplacian because in our case the fungal growth didn't have a definite shape. So, this laplacian filter can detect edges in all directions simultaneously.



After applied the laplacian filter we subtracted from previous output and got sharpened images as shown as below.





So, these are the steps that conclude the algorithm of the pre-processing phase. 
 
This is the simple overview of our pre-processing phase.
 
	

