---
layout: post
title:      "Let's hash it out"
date:       2018-02-10 09:56:40 -0500
permalink:  nested_hashes
---



Hash Facts:
 
   * Hashes are key/value pairs that can be made up of strings, symbols or integers.

   * Every key in a hash needs to be unique or else the duplicate key can override and replace the existing key. 

   * Hashes have no beginning or end.  Unlike an array the key/value pairs can't be appended '<<' to a hash, they need to   
     be inserted
	 
 
 
How to create a hash
                                                
																																	
class constructor                                                                             

    shop = Hash.new                                                                                        

     shop["vegetable"] = "onion"                                                                                 
     shop["fruit"] = "apple"                                                                                              
     shop["drink"] = "sprite"                                                                                            
                                                                                                                                        
      puts shop["drink"]                                                                                       
         => "sprite"



literal constructor- literally (inline) with brace

    shop = {
      "vegetable": "onion",
	  	"fruit": "apple",																							
      "drink": "sprite"
         }
    puts shop[:"drink"]
      => "sprite"
	 
	 
	 
Hashes store data in keys and can be assessed by the key name:


    shop = {"vegetable" => "onion", "fruit" => "apple", "drink" => "sprite"} 

    shop["fruit"]

         =>"apple


Adding a new key/value pair


                    shop["dairy"] = "butter"


                               puts shop

                                      => {"vegetable"=>"onion", "fruit"=>"apple", "drink"=>"sprite", "dairy"=>"butter"}




Hashes have a default value of nil.  Therefore nil is returned when searching for a key that doesn't exist.  
Change the default value by sending it as an argument 

    shop = Hash.new("nope")          Now default value is now "nope" instead of nil 


    shop["vegetable"] = "onion"
    shop["fruit"] = "apple"
    shop["drink"] = "sprite"
 
    puts shop["meat"]      

        => returns "nope"
  


Symbols 


Why are they used? 
      
Stings are mutable.  Every time a new string is created a new object id is made, even if an identical string is created.  This is because strings are saved in 2 different locations in memory.

Symbols are immutable.  You will always get the same object id no matter how many times you use that particular symbol. 

String 

    name = "Steven"                                                                                                 
    same_as_name = "Steven"                                                                             

    name.object_id == same_as_name.object_id                                        
     => false                                                                                                            


    puts "Steven".object_id                                                                                    
    puts "Steven".object_id                                                                                    
    puts "Steven".object_id                                                                                    
 
    => 70236825545220                                                                                       
    = > 70236822108160                                                                                     
    = > 70236821810060                                                                                      

Symbol

    name = :steven
    same_as_name = :steven

    name.object_id == same_as_name.object_id
     => true

    puts :steven.object_id
    puts :steven.object_id
    puts :steven.object_id
    => 1093988
    => 1093988
    => 1093988



Types of symbols:

       numbers = {:first => "one"}     is equal to   number = {first: "one"}

       The key first: is still interpreted as a symbol by the interpreter.

       Either syntax can be used as long as you're consistent and stick to one. 












