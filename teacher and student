/*There are 3 student processes and 1 teacher process. Students are supposed to do their assignments and they need 3 things for that pen, paper and question paper.
The teacher has an infinite supply of all the three things. One students has pen,an other has paper and another has question paper. 
The teacher places two things on a shared table and the student having the third complementary thing makes the assignment and tells the teacher on completion.
The teacher then places another two things out of the three and again the student having the third thing makes the assignment and tells the teacher on completion.
This cycle continues. Write a programme to synchronize the teacher and the students.*/
#include<stdio.h>
#include<stdbool.h>
struct apparatus
{
 	bool pen ;
	bool paper ;
	bool question_paper ;
	bool all_three_students ;
};
int main()
{
	int n=3;
	struct apparatus  a[n];
	a[0].pen=true;		
	a[0].paper = false;
	a[0].question_paper = false;
	a[0].all_three_students= false;
	a[1].pen=false;		
	a[1].paper = true;
	a[1].question_paper = false;
	a[1].all_three_students = false;
	a[2].pen=false;		
	a[2].paper = false;
	a[2].question_paper = true;
	a[2].all_three_students = false	;
	while(a[0].all_three_students==false||a[1].all_three_students==false||a[2].all_three_students==false)
	{
		int b1,b2;
		printf("\n Assigned things:\n1.pen\n2.paper\n3.question paper\n Enter the two things that are placed on the shared table: ");
		scanf("%d%d",&b1,&b2);
		if(b1==1 && b2==2 &&  a[2].all_three_students==false)
		{
			a[2].all_three_students=true ;
			printf("1st Student completed the task\n");
		}
		if(b1==2 && b2==3 && a[0].all_three_students==false)
		{
			a[0].all_three_students=true;
			printf("2nd Student completed the task\n");
		}
		if(b1==1 && b2==3 && a[1].all_three_students==false)
		{
			a[1].all_three_students=true;
			printf("3rd Student completed the task\n");
		}
		if(b1>=4 && b2>=3)
		{
			printf("enter the correct input\n");
		}
	}
	printf("All the students successfully completed their project\n");
	return 0;
}
