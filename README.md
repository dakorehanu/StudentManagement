# StudentManagement
This is repository for education Purpose
<br>
Author-Hanuman Dakore
<br>
package com.sorting;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.Map.Entry;

public class MapSort1 {

	
	
	public static void main(String[] args) {
		
		
		Map<String, Integer> map=new HashMap<>();
		
		map.put("ten", 10);
		map.put("thirty", 30);
		map.put("elevan", 11);
		map.put("five", 5);
		map.put("fifty", 50);
		map.put("twenty", 20);
        map.put("forty",40);
		
		List<Entry<String, Integer>> entries=new ArrayList<>(map.entrySet());
		
		Collections.sort(entries,( o1, o2) ->o1.getValue().compareTo(o2.getValue()));
		
		for (Entry<String,  Integer> entry:entries) {
			System.out.println(entry.getKey()+"   "+entry.getValue());
		}
		
	map.entrySet().stream().sorted(Map.Entry.comparingByKey()).forEach(System.out::println);
	System.out.println("******************************************************************");

	map.entrySet().stream().sorted(Map.Entry.comparingByValue()).forEach(System.out::println);
		
	}
}

