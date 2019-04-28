
mybatis中用到了哪些设计模式？
1.SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
在创建SqlSessionFactory时用到了建造者模式和单例模式。
2.BlogMapper mapper = session.getMapper(BlogMapper.class);
在SqlSession.getMapper时，其实获取到的是代理对象。MapperProxy 。用到了代理模式。
3.在创建执行器Executor时，有三种Executor。他们都继承自BaseExecutor 。这里用到了模板方法模式。
