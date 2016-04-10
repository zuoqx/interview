##1.0 内存不足时，系统会杀死台的Activity,若需要保存状态，在哪个方法里进行？  
>   **onInstanceState(Bundle)** 在Activity在即将被kill掉的时候会调用，用来保存一些状态信息。在onCreate或者onRestoreInstanceState(Bundle)方法里恢复这些状态信息（保存在Bundle里）  
>   在onStop()之前会被调用，但不能保证在onPause的前后被调用。  
>   **onRestoreInstanceState(Bundle)**  在 onStart() 和 onPostCreate(Bundle)直接被调用  
>                   大多数情况下，在onCreate(Bundle)恢复状态