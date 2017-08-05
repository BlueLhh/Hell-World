# Hell-World
package com.homework.lhh;

import java.util.InputMismatchException;
import java.util.Scanner;

public class Ex02 {
	@SuppressWarnings("resource")
	public static void main(String[] args) {
		int[] array = new int[5];
		Scanner sc = new Scanner(System.in);
		int num;
		System.out.println("请输入五个字符：");
		try{
			for (int i = 0; i < 10; i++) {
				System.out.print("请输入第"+(i+1)+"位字符：");
				num = sc.nextInt();
				array[i] = num;
			}
		}catch(InputMismatchException e){
			System.out.println("请输入整数！");
		}catch(ArrayIndexOutOfBoundsException e){
			System.out.println("输入整数个数不能超过5个");
		}catch(Exception e){
			e.printStackTrace();
		}		
		for (int i = 0; i < array.length; i++) {
			System.out.print(array[i]+" ");
		}
	}
}
