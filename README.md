# StringToCollectionRepo
    package com.Assignment;

		import java.util.*;
		import java.util.Map.Entry;
		
		public class StringOverloading {
			
		public  static void StrOverloading()
			{
				String str="Fname=IISAC|LName=Newton|Address=UK|Age=20|School=Trinity|Invention=LawsOfMotion";
				Map<String,String>map =new LinkedHashMap<String,String>();
				
				String []split=str.split("\\|");
				for(String singleKey : split)
				{
					String[] KeyVal=singleKey.split("=");
					map.put(KeyVal[0], KeyVal[1]);
				}
				
				for(Entry<String,String> entry: map.entrySet())
				{
					System.out.println(entry.getKey()+":"+entry.getValue());
				}
			}
			
			public static void main(String[] args) 
			{
				
				StrOverloading();
			}
		
		}

