# preparation
#include<stdio.h>
int findNum(int num);  // Declare the function

 
void main() {

	int num = 355669;
	int missing = findNum(num);
	printf("%d\n", missing);
}



int findNum(int num) {

	int answer = 0;
	if (num < 10) {
		return 0;
	}
	int num1 = num % 10;
	int num2 = num % 100/10 ;
	 
	if (num2 > num1) {
		answer++;
	}
	answer = answer + findNum(num / 10);

	return answer;
}
