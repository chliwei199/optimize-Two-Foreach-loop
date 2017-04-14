## How to optimize two foreach loop to one? 

if you have the $array=[$A,$B,$C,$D,$E,$F]. Furthermore, you want to find which one is the 

biggest in array And need to use this number to calculate with the user send 

the number from webSite.

How can I reduce two foreach loop to one?? 

* Brute Force:

```php
    $Maximum=1;
    $Chooice=0;
    foreach($array as $arrayElement){
        if($arrayElement->number > $Maximum){
        $Maximum=$arrayElement->number;
        }
    }
    foreach($array as $arrayElement){
        if($arrayElement->number===$userChoose){
        $Maximum = $Maximum / $arrayElement->number;
        }
    }

```
###### **ThereFore you can get the two parameters. But how can I optimize???


* Optimize:

```php
   $Maximum=1;
   $Chooice=0;
    foreach($array as $key=>$arrayElement){
        if($arrayElement->number > $Maximum){
        $Maximum=$arrayElement->number;
        }
        if($arrayElement->number===$userChoose){
         $Chooice=$arrayElement->number;
        }
    }  
    $Maximum= $Maximum/$arrayElement[$Chooice]->number;
    
```
####  **Therefore I only use one foreeach to complete the same thing.