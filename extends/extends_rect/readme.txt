1.菱形继承会出现顶部类重定义问题，解决此问题可以使用#ifndef解决，在创建类的时候ide已经帮我们生成好了，所以建类的时候尽量不要copy其它的类，以免造成#ifndef失效。
2.虚析构函数的作用是当用一个基类的指针删除一个派生类的对象时，派生类的析构函数会被调用。
3.菱形继承的问题，会导致存在多个顶层类的对象，解决方式是通过虚继承。
    Person()
    Framer()
    Person()
    Worker()
    MigrantWorker()
    ~MigrantWorker
    ~Worker()
    ~Person()
    ~Framer()
    ~Person()