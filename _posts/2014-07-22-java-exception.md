---
layout: post
title: Java异常学习笔记
categories: tech
tags: java,Exception
---

有效处理Java异常三原则 

1. 具体明确

```

   File prefsFile = new File(prefsFilename);
    
   try{
       readPreferences(prefsFile);
   }
   catch (FileNotFoundException e){
       // alert the user that the specified file
       // does not exist
   }
   catch (EOFException e){
       // alert the user that the end of the file
       // was reached
   }
   catch (ObjectStreamException e){
        // alert the user that the file is corrupted
   }
   catch (IOException e){
       // alert the user that some other I/O
       // error occurred
   }
   
```

2. 提早抛出

```
  public void readPreferences(String filename)
  throws IllegalArgumentException{
      if (filename == null){
           throw new IllegalArgumentException("filename is null");
      }  //if
   
     //...perform other operations...
   
     InputStream in = new FileInputStream(filename);
   
     //...read the preferences file...
  }
```

3. 延迟捕获

```
   public void readPreferences(String filename)
   throws IllegalArgumentException,
   FileNotFoundException, IOException{
       if (filename == null){
              throw new IllegalArgumentException("filename is null");
        }  //if
    
        //...
    
        InputStream in = new FileInputStream(filename);
    
   //...
   }
