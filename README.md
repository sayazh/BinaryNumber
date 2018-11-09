# BinaryNumber
BinaryNumber
import java.util.Arrays;
import java.util.Scanner;

public class BinaryNumber {

	public static void main(String[] args) {

		/*
		 * Given an array binary with 8 integers (0s or 1s), write java program to
		 * calculate decimal value and print out to console. Feel free to use additional
		 * arrays or formulas.
		 */
		Scanner input = new Scanner(System.in);

		int[] binary = new int[8];
		for (int i = 0; i < binary.length; i++) {
			binary[i] = input.nextInt();
		}

		int decimal = 0;
		for (int i = binary.length - 1; i >= 0; i--) {
			if (binary[i] == 1) {
				decimal += Math.pow(2, binary.length - i - 1);

			}
		}
		System.out.println("The decimal value of binary ->"+Arrays.toString(binary));
		System.out.println(decimal);
		input.close();
	}
}
