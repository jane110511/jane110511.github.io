---
layout: post
title: Merge Sort
categories: Technology
tags: algorithms sort
---

Merge Sort
===
- Java sort for objects
- Divide array into two halves
- Take an auxiliary array to hold the data

- MergeSort implement by Java

```
public class Sort {
	private static boolean isSorted(Comparable[] a, int lo, int hi) {
		for(int i = lo; i < hi; i++){
			if (a[i].compareTo(a[i+1]) > 0){
				return false;
			}
		}
		return true;
	}

	private static void merge(Comparable[] a, Comparable[] aux, int lo,
			int mid, int hi) {
		assert isSorted(a, lo, mid);
		assert isSorted(a, mid + 1, hi);
		//copy
		for (int i = lo; i <= hi; i++) {
			aux[i] = a[i];
		}
		//merge
		int i = lo, j = mid + 1;
		for (int k = lo; k <= hi; k++) {
			// forget to add the condition of exhausted array
			if (i > mid) {
				a[k] = aux[j++];
			} else if (j > hi) {
				a[k] = aux[i++];
			} else if (aux[i].compareTo(aux[j]) <= 0) {
				a[k] = aux[i];
				i++;
			} else {
				a[k] = aux[j];
				j++;
			}
		}
		assert isSorted(a, lo, hi);
	}
	
	private static void sort(Comparable[] a, Comparable[] aux, int lo,
			int hi){
		//need to add return condition
		if(lo >= hi) return;
		int mid = lo + (hi - lo)/2;
		sort(a, aux, lo, mid);
		sort(a, aux, mid +1, hi);
		merge(a, aux, lo, mid, hi);
	}
	
	public static void sort(Comparable[] a){
		int lo = 0, hi = a.length;
		Comparable[] aux = new Comparable[hi];
		sort(a, aux, lo, hi-1);
	}
	
	public static void main(String[] args){
		String[] a = {"2","3","4","1","3","0","9","8","7","5","5"};
		sort(a);
		for(String s : a){
			System.out.println(s);
		}
 	}

```

Assertion
==
- Helps detect logic bugs
- Documents code
- Enable or disable at runtime

```
java -ea MyProgram //enable assertions
java -da MyProgram //disable assertions(default)
````



	