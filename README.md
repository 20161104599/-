# -
#include "stdafx.h"
#include<iostream>
using namespace std;

struct student
{
	char name[20];
	char num[15];
	int age;
	struct student *next;
};

int main()
{
	struct student *p,*q,*head;
	int s=1;
	p=new student;
	q=p;
	head=q;
	cout<<"please input data;"<<endl;
	cin>>head->name;
	cin>>head->num;
	cin>>head->age;
	while(cout<<"1 or 2?",cin>>s,s==1)
	{
		p=new student;
		q->next=p;
		q=p;
		cin>>p->name;
		cin>>p->num;
		cin>>p->age;
		if(head=NULL)
		{
			head=p;
		}
		else
		{
			q->next=p;
		}
		q=p;
		p->next=NULL;
	}
	p=head;
	while(p!=NULL)
	{
		cout<<p->name<<" "<<p->num<<" "<<p->age<<endl;
		p=p->next;
	}
	return 0;
}
