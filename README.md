#include<stdio.h>

int findNum(int num, int big);  // Declare the function

int main() {
	int num = 977977;
	int big = 7;
	int missing = findNum(num, big);
	printf("%d\n", missing);
}

int findNum(int num, int big) {
	int sum = 1;
	int n = num % 10;
	
	if (num < 10) {
		return 0;
	}

	if (n == big) {
		sum = 1;
	}
	else
		sum = 0;

	sum = sum+ findNum(num / 10, big);  // Corrected line

	if (sum % 2 == 0) {
		return 1;
	}
	return 0;  // Added return statement
}
