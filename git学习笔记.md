> #### ��װGit��Windows��

��[https://git-for-windows.github.io](https://git-for-windows.github.io/)����git���а�װ��Ȼ�������Ҽ�����ҵ�git bash here�������Ҫ�Ǳĳ�һ�������������д��ڵĶ�������˵����װ�ɹ���
Ȼ�����һϵ�����ã������������룺
<code> git config --global user.name "Your Name"
&nbsp;$ git config --global user.email "email@example.com"</code>

> #### �����ֿⲢ��git bash�ϴ��ļ������زֿ�

1. ����ѡ��һ�����ʵĵط�������һ����Ŀ¼��
<code> 
mkdir learngit
cd learngit
pwd
</code>
pwd����������ʾ��ǰĿ¼��
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-c8c61fc0c4054651.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2. ͨ��git init������Թ���ֿ⡣
�����ʹ�������һ���ֿ⣬���Ǵ�Ŀ¼�»����һ��.git�ļ������ܽ����޸ģ�������ƻ��ֿ⣬Ҳ�п������أ����صĻ�������������ls -ah����ͻ���֡�
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-14653710abba8798.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
3. ���ͨ��git����һ��.md�ļ���
git bash��touch xxx.md��vim xxx.md ���������ļ�λ��git bash�򿪵�λ�á�
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-13a8742c853832fa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
4.��ν��ļ��ϴ����ֿ⣿
��һ������git add�������git����ļ���

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-54df08e44fd6d7ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
�ڶ��� ��git commit�������git ���ļ��ύ���ֿ�

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-6e755fb4bc9b1cd2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
######ΪʲôGit����ļ���Ҫadd��commitһ�������أ���Ϊcommit����һ���ύ�ܶ��ļ�����������Զ��add��ͬ���ļ������磺
<code>
$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."
</code>

> #### git������¼

֮ǰ�Ѿ��ύ��һ��gitѧϰ�ʼǵ��ļ�,���ڿ��Զ�������޸ġ�
1. ͨ�� git status�������ʱ�����ղֿ�Ķ�̬��
2. ͨ��git diff������Բ鿴�Բֿ���޸ļ�¼��
3. ͨ��git long������Բ鿴�ڱ��زֿ��е����в�����¼��
4. �����Ҫ�ɵ�ǰ�ļ��˻ص��������޸Ĺ�����ļ�������ͨ��<code>git reset -hard HEAD^</code>��ʵ�֣�����������޸ļ�¼����Ҫ�˻ص�����֮ǰ���ļ�������<code>git reset -hard HEAD^^</code>�����Ҫ�˻ص�����ǰ�ͼӼ���<code>^</code>,�������̫�಻��д���Ϳ���д��<code>git reset -hard HEAD~n</code>.
5. git reflog����������¼���ÿһ������ģɣĺš�
###### ������ÿ���޸��ļ����󣬶���Ҫ��<code>git add</code>������ļ�����һ����ӣ����ļ���ӵ��ݴ�����ֻ������<code>git commit</code>���ܼ�¼�ļ��Ĳ�����¼��
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-ed97aad0f8984f46.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
6. �����޸�
-ֻ�ǽ������޸Ļ�û�зŵ��ݴ���������ͨ��<code>git checkout -- gitѧϰ�ʼ�</code>���Գ������ļ�����һ���޸ġ�
-�������޸Ĳ��ҷŵ����ݴ�������ô����ͨ��<code>git reset HEAD file gitѧϰ�ʼ�.md</code>�Ѷ��ļ����޸ĳ��������ҷŵ���������
7. ɾ���ļ�
-ֱ�����ļ���������ɾ����
-��<code>git rm file</code>�������ɾ����
�Ӱ汾����ɾ�����ļ����Ǿ�������git rmɾ��������git commit��

> #### ���Զ�̿�

�ڱ��ش�����һ��Git�ֿ��������GitHub����һ��Git�ֿ⣬�������������ֿ����Զ��ͬ����������GitHub�ϵĲֿ�ȿ�����Ϊ���ݣ��ֿ�����������ͨ���òֿ���Э��������һ�ٶ�á�
- �ѱ��ؿ���������͵�Զ�̣���<code>git push</code>���ʵ�����ǰѵ�ǰ��֧master���͵�Զ��
######�����ύԶ�̴���������<code>git push -f</code>��OK�ˡ�

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-e8f8821873fde525.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- ��Զ�̿��¡�����زֿ�
����Ҫ�½�һ��Զ�̿⣬Ȼ��ͨ��<code>git clone</code>������п�¡����Զ�ɲֿ⣬��¡�����زֿ⡣
<code>$ git clone git@github.com:Liyinzhe/BIubiubiu.git</code>




