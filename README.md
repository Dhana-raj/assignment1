//*************M.DHANARAJU**************//
#include <stdio.h>
struct student
{
int rollno,tot;
char name[10];
char addr[10];
int marks[5];
float perc;
};
void main()
{
struct student s[5];
int i,n,j;
printf("Enter the number of students:");
scanf("%d",&n);
for(i=0;i<n;i++)
{
printf("\nEnter Student Roll Number: ");
scanf("%d",&s[i].rollno);
printf("\nEnter Student name: ");
scanf("%s",s[i].name);
printf("\nEnter Student addr: ");
scanf("%s",s[i].addr);
printf("\nEnter Student total subject's marks:");
for(j=0;j<4;j++)
scanf("%d",&s[i].marks[j]);
}
for(i=0;i<n;i++)
{
s[i].tot=0;
for(j=0;j<4;j++)
s[i].tot = s[i].tot+ s[i].marks[j];
}
  s[i].perc=(float)((float)s[i].tot/(float)500)*100;
for(i=0;i<n;i++)
{
printf("\nStudent Roll no. – %d", s[i].rollno);
printf("\nStudent Name – %s", s[i].name);
printf("\nStudent addr – %s", s[i].addr);
printf("\nStudent Total Marks – %d", s[i].tot);
printf("\nStudent  percentage  – %f ",s[i].perc);
}
}
