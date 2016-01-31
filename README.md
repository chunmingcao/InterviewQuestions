# InterviewQuestions

## Implement Singleton  

  class CollabController{
  
      private static CollabController instance;
  
      public static CollabController getInstance(){
      
          if(instance == null){
              synchronize(CollabController.class) {
                  if(instance == null){
                      instance = new CollabController();
                  }  
              }          
          }
          return instance;
      }
  }

## Implement Stack

  class Stack<T>{
  
      private T[] data;
      private static final DEFAULT_LENGTH = 100;
      private length;
      
      private index;
      
      public Stack<T>(){
          data= new T[DEFAULT_LENGTH ];
          index = -1;
          length = DEFAULT_LENGTH ;
      }
      
      public Stack<T>(int length){
          data= new T[length];
          index = -1;
          this.length = length ;
      }
      
      public push(T e) throws{      
          synchronize(this){
              if(index >= length-1 ){
                  throw new Exception("xxxdata");
              }
              data[++index] = e; 
          }  
      }
      
      public T pop(){   
          synchronize(this){
              if(index < 0){
                  return null;
              }
              data[index --] = null; 
          }       
      }
  }
  
## How to keep a program keep running with minimun resource?
  
    sychronized(this){
      this.wait();
    }
  
## RESTful service trasaction
  
   debtAccountService
   withraw
   deposit
   
   
   
