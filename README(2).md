 [youtube] https://www.youtube.com/channel/UCZCFT11CWBi3MHNlGf019nw/search?query=time%20complexity
 
 [time complexity and space complexity] https://lnkd.in/dJ7m5-bu

# Time complexity of For loop 
    for(i=0;i<n;i++)          ----->  O(n)
    for(i=0;i<n;i=i+2)        ----->  n/2*O(n)
    for(i=n;i>i;i--)          ----->  O(n)
    for(i=1;i<n;i=i*2)        ----->  O(logn base2)
    for(i=1;i<n;i=i*3)        ----->  O(logn base3)
    for(i=n;i>1;i=i/2)        ----->  O(logn base2)
    
    
    
    
    1) for(=0;i<n;i++)           ---> n+1
       {
           for(j=0;j<n;j++)      ---> n(n+1)
           {
           #stmt                 ---> n*n
           }
       }                  =======>>  O(n^2)
    
    
    
     2) for(i=0;i<n;i++)           
        {
            for(j=0;j<i;j++)
            {
            #stmt
            }
         }                 1+2+3+4.....+n = n(n+1)/2 =n^2 
                          =======>>  O(n^2)
       
       
                          
      3) p=0;
         for(i=1;p<=n;i++)       -------> 1 2 3 4.....k
         {
            p=p+i;               --------> 1 3 5 10.....k
          }
          #assume  p>n
                   p=k(k+1)/2
                   k(k+1)/2 < n
                   k^2 > n
                   k > rootof(n)   ======>> O(rootof(n))
          
          
          
         4) for(i=0;i<n;i++)         -----> n
            {
            #stmt
            }
            for(j=0;j<n;j++)          -----> n
            {
            #stmt
            }                           =======>> O(n)
          
          
          
          5) p=0
          for(i=1;i<n;i=i*2)
          {
          p++                        ------> log n
          }
          for(j=1;j<p;j=j*2)
          {
          #stmt                       ------> log p
          }                           ========>> O(log(logn))
                   
                   
           
           
           6) for(i=0;i<n;i++)        ----> n
              {
              for(j=1;j<n;j=j*2)       ----> n*logn
              {
              #stmt
              }                       -------> n*log n
              
              2n*log n + n = O(n(log n))
              
                   
                   
