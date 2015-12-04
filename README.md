class List{
public:
	double* data;
	int* pos;
	int prev;
	int curr;
	int prevE;
	int currE;
	List(int n);
	void MoveNext();
	void Add(double k);

private:
	void Del_Node(int t);
	void Add_Node(int t);
}








#include "List.h"
List :: List(int n){
	data = new double[n];
	pos = new int[n];
	pos[0] = 0;
	for(int i = 1; i < n - 2; i++)
		pos[i] = i + 1;
	pos[n - 1] = 1;
	curr = 0;
	prev = 0;
	currE = 1;
	prevE = n - 1;
}

void List::MoveNext(){
	prev = curr;
	curr = pos[curr];
}

void List::Add(double k){

}

void List::Del_Node(int t){
	pos[t] = 

}
