//# forward-list-stl-c-stl-
//forward list stl c++ | Библиотека стандартных шаблонов (stl). Обучение С++
#include<forward_list>
using namespace std;
int main()
{
	forward_list<int> fl = { 137,89,26 };
	fl.push_front(1);
	fl.push_front(4);//добавили в начало

	for (auto el:fl)//вывели элемент из объекта fl, см урок137
	{
		cout << el << endl;
	}
	forward_list <int> ::iterator it = fl.begin();//создали итератор
	it++;//сдвигаем на след эл-т
	//it--; так нельзя, т к декремент не перегружен т к мы работаем с односвяз списком
	cout << *it << endl;
	fl.insert_after(it, 999);

	for (auto el : fl)//вывели элемент из объекта fl 
	{
		cout << el << endl;
	}
	//forward_list <int> ::iterator it = fl.before_begin();//поставим эл-т после "ничто"
	//fl.erase_after(it);




	return 0;
}



