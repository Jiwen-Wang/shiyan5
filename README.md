# shiyan5
一、实验目的

·分析学生选课系统

·使用GUI窗体及其组件设计窗体界面

·完成学生选课过程业务逻辑编程

·基于文件保存并读取数据

·处理异常

二、实验要求

1、系统角色分析及类设计

2、要求

·设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作

·基于事件模型对业务逻辑编程，实现在界面上支持上述操作

·针对操作过程中可能会出现的各种异常，做异常处理

·基于输入/输出编程，支持学生、课程、教师等数据的读写操作

三、实验过程

1.登录——学生

当学生输入正确的用户名和密码时和权限连接到学生界面，进行选课和查看课程操作，如果用户名和密码错误有提示。

2.管理员admin 密码admin

当管理员输入正确的用户名和密码时和权限连接到界面，进行增添课程、删除课程、更新、打印课程信息和查看课程操作，如果用户名和密码错误有提示。

3.初始化学生信息

在users里设置账号密码，以空格分隔

四、实验流程图

见附件

五、核心代码

public void actionPerformed(ActionEvent e) {
				// TODO Auto-generated method stub
				try {
					PrintStream printStream = new PrintStream("所有学生的选课信息.txt");
					System.out.println("user............."+users);
					for(User user: users) {
						printStream.println("学生："+user.getUsername()+"    选课信息：");
						Set<Custom> set = user.getSet();
						for (Custom custom : set) {
							printStream.println(custom);
						}
						printStream.println("---------------------------------------");
					}
					printStream.close();
				} catch (FileNotFoundException e1) {
					// TODO Auto-generated catch block
					e1.printStackTrace();
				}
			}
		});
  
六、程序运行截图

见附件

七、编程感想

通过本次实验我已经掌握了设计GUI界面的方法，学会了组件的布局和这个学期学习的各种各样的知识。在实验中，页面跳转方法是使用较为频繁的方法之一，在页面跳转时要先在需要跳转的页面上添加监听，再连接新的页面。这次的实验难度比较大，在实验过程中遇到了不少问题，通过上网搜索，查找课本，询问同学等方法问题基本得到了解决，这次我也学会了用GitHub上传文件，弥补了上次实验的遗憾。

