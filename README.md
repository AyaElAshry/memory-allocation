# memory-allocation

We have created a struct **location** to deal with each segment a location having its own process name, segment name, base & limit values.  

`struct location  
{                                  
      QString process = "";       
      QString segment = "";        
      int base;      
      int limit;  
      int End() { return base + limit; }  
      int Size() { return  limit; }  
    };`
* The first window takes **the memory size** and **the holes base & limit values**.  
![m3](https://user-images.githubusercontent.com/64116564/83948776-b4c33080-a7ed-11ea-999c-86df4d620c04.png)
* Then, after pressing on "DONE" button.   
-> this will redirect us to the window **where the memory will be drawn** & we can **allocate** and **deallocate** any processes.  
![m1](https://user-images.githubusercontent.com/64116564/83948816-0c619c00-a7ee-11ea-99d7-09d62a68bba3.png)
* You have to choose **the Allocation Method (Best-Fit or First-Fit)**, after entering the data of the process and its segments the process will be allocated directly and showed in the memory layout & also it will be showed in the tree view and by selecting it, its internal data will appear in the segment table.   
**-> First-Fit allocation method is used here.** 
![m4](https://user-images.githubusercontent.com/64116564/83948847-3a46e080-a7ee-11ea-9c38-e0e758438968.png)
**-> Best-Fit is used here.**   
![m5](https://user-images.githubusercontent.com/64116564/83948887-842fc680-a7ee-11ea-96b2-e41c43f9d803.png)
* To **deallocate** a process by **all its segments**, you only have to select the process from **the tree view** and press on "Deallocate" button.  
![m6](https://user-images.githubusercontent.com/64116564/83948917-b80aec00-a7ee-11ea-8865-548ba629c367.png)
