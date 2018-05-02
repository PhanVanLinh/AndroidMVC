# AndroidMVC

On internet, THERE ARE MANY IDEA to implements MVC from different people

**Example**
1) Some people say Android itself is MVC. (*it is very old so I think we should not care this way*)   
**Model**: Class handle business, handle database, API  
**View+Controller**: Activity+Fragment

2) Separate Activity  
**Model**: Class handle business, handle database, API   
**View**:  Activity or Fragment  
**Controller**:  A separate classes that don’t extend or use any Android class.  
*This way is quite similar to MVP, however it have some thing different*

## Basic of MVC

#### 1) Passive Model  
User interact on **View**, **View** send action to **Controller**.  
**Controller** control **Model**.  
After **Model** update finish, **Controller** will notify to the **View**.  
**View** will get data from **Model** then update the UI. 

#### 2) Active Model  
> The different to Passive Model is: View will observe Model changed (by use Observer pattern). It don't need to receive notify from Controller
 
User interact on **View**, **View** send action to **Controller**.  
**Controller** control **Model**.  
**View** observe on **Model** change then update UI

## Different between MVC and MVP

**View** in MVP: Only display data (**View** don't know **Model**). **Presenter** control **View** to display data.  
**View** in MVC: Receive notify from **Controller** and then get data from **Model** to display.  


## Disadvantage
#### No where to put UI Logic
If we put UI logic in **Model** => **Model** contain both UI logic and business logic => not good  
If we put UI logic in **View** (example Activity) => **View** do logic => not good  

## Reference
https://medium.com/upday-devs/android-architecture-patterns-part-1-model-view-controller-3baecef5f2b6
https://www.techyourchance.com/mvp-mvc-android-1/