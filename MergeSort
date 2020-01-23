package com.company;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class Main {

    public static void main(String[] args) {

        List<Integer> array = new ArrayList<>();
        array.add(4);
        array.add(2);
        array.add(1);
        array.add(3);
        array.add(5);
        array.add(6);

        long startTime = System.currentTimeMillis();
        array = mergeSort(array);
        long endTime = System.currentTimeMillis();
        long duration = (endTime - startTime);
        System.out.println(array + "   " + duration);

    }

    private static List<Integer> mergeSort(List<Integer> array) {
        // if array is equal = 1, stop splitting
        if(array.size() <= 1) return array;

        int midPoint = array.size() / 2;
        List<Integer> left = new ArrayList<>();
        List<Integer> right = new ArrayList<>();

        for (int i = 0; i < midPoint; i++) {
            left.add(array.get(i));
        }

        for (int j = midPoint; j < array.size(); j++) {
            right.add(array.get(j));
        }

        left = mergeSort(left);
        right = mergeSort(right);

        return merge(left, right, array);

    }

    private static List<Integer> merge(List<Integer> left, List<Integer> right, List<Integer> array) {

        int leftPointer = 0;
        int rightPointer = 0;
        int resultPointer = 0;

        while( leftPointer < left.size() || rightPointer < right.size() ) {

            if( leftPointer < left.size() && rightPointer < right.size() ) {

                if( left.get(leftPointer) < right.get(rightPointer) ) {
                    array.set(resultPointer++, left.get(leftPointer++));
                } else {
                    array.set(resultPointer++, right.get(rightPointer++));
                }

            } else if( leftPointer < left.size() ) {

                array.set(resultPointer++, left.get(leftPointer++));

            } else {

                array.set(resultPointer++, right.get(rightPointer++));

            }

        }

//        System.out.println( left + " " + right + " " + array);
        return array;

    }

}
