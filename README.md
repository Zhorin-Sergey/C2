template <class val>
bool comp(List<val> a, List<val> b) {
	if(a.pFirst == 0 && b.pFirst == 0)
		return true;
	if(a.pFirst == 0 || b.pFirst == 0)
		return false;
	Node<val> *f1 = a.pFirst;
	Node<val> *f2 = b.pFirst;
  while (f1->next != 0) {
    if (f1->key != f2->key)
      return false;
    f1 = f1->next;
    f2 = f2->next;
  }
  return true;
}

template <class val>
class Node {
public:
	Node<val>* next;
	val key;
};

template <class val>
class List {
protected:
	Node<val>* pFirst;
public:
	~List();
	void Insert(Node<val>* a);
	Node<val>* search(val t);
	void print();
	Node<val>* Delete(val t);
	void Insert1(Node<val>* a, val t);
};

template <class val>
class Stack {
private:
	List<val>* l;
public:
	~stack(){
		delete l
	};
	int IsFull()const {
		Node<val>* tmp;
		try {
			tmp = new Node<val>;
		}
		catch(..) {
			return 1;
		}
		delete tmp;
		return 0;
	};
	int IsEmpty()const {
		return(comp(l,0));
	};

	void Push(val t) {
		if(IsFull())
			return;
		Node<val>* tmp = new Node<val>;
		tmp->key = t;
		Insert(tmp);
	};

	val pop() {
		if(IsEmpty())
			throw "stack is empty";
		Node<val>*f = l.pFirst;
		Delete(f->key);
		val k = f->key;
		delete f;
		return k;
	};
};

