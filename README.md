# Webworker

Some example of worker and sharedworker

Description:
A web worker is a JavaScript running in the background, without affecting the performance of the page.
It runs outside of the main application thread and do not have the same access to JavaScript features as your main application does. 
Your workers do not not have access to:

  1.The DOM
  
  2.The document object
  
  3.The window object
  
  4.The parent object
  

1. Difference between worker and sharedworker: 
    A Worker can only be accessed from the script that created it, 
    A SharedWorker can be accessed by any script that comes from the same domain.
2. workers & Shared workers use slightly different APIs. 

