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

FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF

double List::check1(List a, List b){
  if(a.pos[0] == 0 || b.pos[0] == 0)
    throw exception("At least one of lists empty");
/*  while(a.curr != 0)
	  a.MoveNext();
  while(b.curr != 0)
	  b.MoveNext();*/
  a.curr = 0;
  b.curr = 0;
  a.MoveNext();
  b.MoveNext();
  while(a.curr != 0) {
    while(b.curr != 0) {
	  if(a.data[a.curr] == b.data[b.curr])
		  return a.data[a.curr];
      b.MoveNext();
    }
    a.MoveNext();
	b.MoveNext();
  }
	return 0;
}


TEST(MyList, can_find_equal_element) {
  List a(4);
  List b(5);
  a.Add(12);
  a.MoveNext();
  a.Add(13);
  a.MoveNext();
  a.Add(15);
  b.Add(15);
  b.MoveNext();
  b.Add(12);
  b.MoveNext();
  b.Add(17);
  b.MoveNext();
  b.Add(16);
  List l(1);

 // double t = l.check1(a, b);
 /* double t = List::check1(a, b);
  EXPECT_EQ(12, t);*/
}
