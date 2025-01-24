### CSR: Communication Between Processes

I've never explained it and won't now too, but CSR is designed to run multiple
processes at the same time, whether it be an illusion or a literal multithreaded
design. In any case those processes somehow need to communicate with each other.
I plan to implement (actually I am implementing it currently) a messaging system 
to allow the processes to communicate with each other. 

CSR is a multi-layered runtime. It's structure is like this:

```
VM  
|_ Assembly  
|_ Assemlby  
|   .  
|   .  
|   .  
|   .  
|_ Assembly  
    |_ Board  
    |   .  
    |   .  
    |   .  
    |   .  
    |_ Board  
        |_ Process  
        |   .  
        |   .  
        |   .  
        |   .  
```

Messages can be sent to either the component right above you or the component right
below you. If you want to send a message to any other component, you have to send it
to one of these first, and request a redirect. 

The basics of the messaging system is this. I'll explain it in more detail in CSR
documentation.
