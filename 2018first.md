# preparation
#include<stdio.h>
int findNum(int num);  // Declare the function


void main() {

	int num = 124; 
	int missing = findNum(num); 
	printf("%d\n", missing); 
}


int findNum(int num) {

	if (num < 100) {
		return 1;
	}
	int a = num / 100 % 10;
	int b = num / 10 % 10;
	int c = num % 10;

	if (!((a < b && b > c) || (a > b && b < c))) {
		return 0;
	}
	return findNum(num / 10);
}
