## Last Update

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

## History

- [CSR Communication Between Processes](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/CSR_Communication_Between_Processes.md) - [25/01/2025]
- [JASM Fixes and CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/JASM_Fixes_and_CSR.md) - [23/01/2025]
- [Current State of CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Current_State_of_CSR.md) - [04.01.2025]
- [About JASM and CSR](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/About_JASM_and_CSR.md) - [10.12.2024]
- [Most Recent Update Is Now Shown On README](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Most_Recent_Update_Is_Now_Shown_On_README.md) - [28.08.2024]
- [About CSLB](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/About_CSLB.md) - [28.08.2024]
- [Now With the Dates](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Now_With_the_Dates.md) - [28.08.2024]
- [Initial Update and Updates Page](https://github.com/The2ndSlimShady/The2ndSlimShady/blob/master/updates/Initial_Update_and_Updates_Page.md)
