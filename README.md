# preparation
#include<stdio.h>
int findNum(int num);  // Declare the function

int main() {
	int num = 69438;
	int missing = findNum(num);
	printf("%d\n", missing);
}

int findNum (int num) {
	int temp = 0;
	if (num < 10) {
		return 1;
	}
	if (num < 1000) {
		int a = num / 100 % 10;
		int b = num / 10 % 10;
		int c = num % 10;
		//temp=
		if (a < b && b > c) {
			return 1;
			
		}

		if (a > b && b < c) {
			return 1;
		}
		return 0;
	}
	return findNum(num / 10);
