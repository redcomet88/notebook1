# Idea导入Eclipse非Maven项目的方法（jgj项目）

---

### 配置步骤

- 使用Idea打开.project文件，等待项目加载完成
- CTRL+ALT+SHIFT+S 进入Project Structure，修改**Project选项卡** Project compiler output为D:\workspace_idea\jgj\WebContent\WEB-INF\classes
- 修改**Modules选项卡** 的第二个标签Paths compile output path 同样和Project中设置一样
- 修改**Modules选项卡** 的第三个标签Dependencies ，把其中不能识别的红色部分删除，并且把引入的jar包全部都删除掉
- 修改**Libraries选项卡**，导入WebContent\WEB-INF\lib，这样做的好处是新的jar包导入只需要放在这个目录下即可，可以被自动引入
- 修改**Facets选项卡（配置让Idea识别项目使用的框架技术）** ,选择正确的web.xml的位置
- 修改**Artifacts选项卡** ,增加 jgj:Web exploded ，输出路径改成 D:\workspace_idea\jgj\WebContent 根目录
- Tomcat 配置Deployment jgj:Web exploded ，Server中的Before Lunch应该会自动出现
- 运行Tomcat

---

### 参考资料

http://wiki.jikexueyuan.com/project/intellij-idea-tutorial/eclipse-java-web-project-introduce.html

````

````