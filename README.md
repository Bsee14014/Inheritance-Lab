# Inheritance-Lab

#include <iostream>

using namespace std;

class band
{	
	protected:
		int count;
	public:
		virtual getcount(int num)
		{
			this->count=num;		
		}
		void print()
		{
			cout<<count<<endl;
		}
		
};

class metalband: public band
{
	public:
		metalband(int no)
		{
			count=no;
		}
		int add()
		{
			count++;
		}
		int remove()
		{
			count--;
		}
		
	private:
		
	
};

class symphony : public band
{
	public:
		symphony(char name[])
		{
			this->name = name;	
		}
	bool update( char name[])
	{
		this->name=name;
	}
	void print()
	{
		cout<<this->name<<endl;
	}
		
		
	private:
		char* name;
	
};
int main()
{
	band b;
	b.getcount(5);
	b.print();
	metalband a(10);
	a.add();
	a.print(); 
	a.remove();
	a.print();
	symphony s("anna");
	s.print();
	s.update("aeni");
	s.print();
	
	
}

