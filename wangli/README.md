GitHub �ʼ�
---
����֪ʶ
---
- **��git����3���������������ݴ����Ͳֿ�**
- **�ڸտ�ʼʹ��git����ʱ��Ҫ���������**
    git config --global user.name ��wangli��
    git config --global user.email ��wangli@gmail.com��**
- cd ..\ ����һ��Ŀ¼
- cd +����:  ����ĳһ����
- cd +�ֿ��� �����Լ��Ĳֿ�
- git add ��file��   �����ļ��ӹ�������ӵ��ݴ���
- git add .   �������ļ���ӵ��ݴ���
- git commit -m �������ļ���ĳһ�����ִ��ݴ�����ӵ��ֿ⣬ÿһ�����ֶ����Ի����о���ð��Լ����޸Ĳ�����Ϊ����
- git diff   �鿴�ȶԱ��޸ĵ����� 
- **���ֻadd��û��commit���������������������git diff �Ժ�û���޸Ĳ��죬Ҳ��˵git diffʵ���ϱȶԵ��ǹ��������ݴ����Ĳ�ͬ**
- git diff-cached �ǲ鿴working tree ��index file�Ĳ��
- git diff HEAD �ǲ鿴working tree ��commit�Ĳ��
- git log   ��ʾ�ӽ���Զ�ύ�Ĳֿ����ʷ��¼
- git init    ����git���Թ���Ĳֿ�
- git checkout +��֧��   ���л���ĳһ��֧
- git reset HEAD file   �ļ����޸ģ�������ӵ��ݴ�����Ҫ�����޸�
- git rm   ɾ���ļ�

��֧����
---
- git branch  �鿴���з�֧,*������ǵ�ǰ���ڵķ�֧��master������֧
- git branch +�ļ���  ������֧
- git checkout name   �л���֧����checkout �����-b��ʾ�������л���֧
- git merge name   �ϲ�ָ����֧����ǰ��֧

���ڱ���������������Ĳ���
---
- �Ȱ�Զ�ֿ̲��¡�����أ��γ��Լ��ı��زֿ�
  git clone +�ֿ��ַ���ֿ��ַ��github����ҳ�С�ATPS clone URL  ������
- �ڰ�note��֧��Զ�ֿ̲���ץ������ץ֮ǰӦ���л���note��֧
  git checkout note
  git fetch origin note
- �ٽ�д�������ύ�����زֿ� ����Ϊmd��ʽ
- ��һ���Ǻϲ��Լ��ķ�֧��note��֧�У������ڵ�ǰ��֧��note�Ļ�����
  git merge wangli --no-ff  **��--no-ff������ʹ����Զ�ֿ̲���Կ����Լ���֧�ϲ��ļ�¼**
- ���һ���������ͣ���Ҫ�ֱ��Լ��ķ�֧��note��֧���͵�Զ�ֿ̲�
  **ע�⣬Ҫ�����ĸ���֧�����Ⱦ�Ҫ�����л����ĸ���֧��**
    git push origin note
    git checkout wangli
    git push origin wangli
    







