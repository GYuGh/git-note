�����汾��
---
- git init    ����git���Թ���Ĳֿ⣬ԭ���Ŀ�Ŀ¼�»�����.gitĿ¼
- git add ��file��   ���ļ���ӵ��ݴ���
- git add .   �������ļ���ӵ��ݴ���
- git commit ���ļ��ύ���ֿ�
- .gitignore   .gitignore���Ժ���һЩ�����ύ���ļ���.gitignore�ļ�����Ҫ�ŵ��汾������Ҷ�.gitignore���汾����

�汾����
---
- git log   ��ʾ�ӽ���Զ�ύ����ʷ��¼������ȷ�����˵İ汾
- git log --pretty=oneline   ������Ϣ����ʾ����ʾ����Ҫ����Ϣ������commit id���ύ������
- git reset   ���˵���һ���汾
- git reset --hard commit id   �ص�ָ���İ汾
- HEAD   ��ǰ�汾��HEAD��   ��һ���汾��HEAD~100   ����100���汾��HEAD��ָ��ǰ�汾��ָ�룬ָ���ĸ��汾�ţ��Ͱѵ�ǰ�汾��λ���ģ�
- git reflog   ��ָ����°汾ʱ��git reflog���Լ�¼�ù���ÿһ������ҵ�Ҫ�ص��汾��commit id

�޸�
---
- git status   �ļ����޸ĺ󣬿����Դ˲鿴��ʱ�����ղֿ⵱ǰ״̬
- git diff   �鿴���屻�޸ĵ����� 
- git checkout --file   �ļ���δ��ӵ��ݴ������������������޸�
- git reset HEAD file   �ļ����޸ģ�������ӵ��ݴ�����Ҫ�����޸�
- git rm   ɾ���ļ�

��֧����
---
- git branch name   ������֧,��checkout�����-d��ʾɾ����֧
- git checkout name   �л���֧����checkout �����-b��ʾ�������л���֧
- git branch   �г����еķ�֧����ǰ��֧ǰ����һ��*
- git merge name   �ϲ�ָ����֧����ǰ��֧
- **�����ͻ**
��master��֧��һ���µķ�֧�ֱ����µ��ύʱ��git���ںϲ�ʱ�������ͻ����Ҫ�ֶ��ı������ٺϲ���
ʵ�ʿ����У��ȶ���master��֧�����ڿ����°汾��ƽʱ�Ĺ���Ӧ�ڲ��ȶ����µķ�֧�ϣ����汾����ʱ�����µķ�֧�ϲ�������֧��
�ϲ���֧ʱ������--no--ff�������Կ����������ϲ���
- **Bug��֧**
���������е�bug����ͨ����ʱ��֧�޸����޸��ϲ��󣬿��Խ���ʱ��֧ɾ����
��ͷ�й���ʱ�������Ȱѹ����ֳ�git stash���������ֳ����أ���bug�޸�����git stash pop,�ָ�stash�����ݵ�ͬʱ����Ҳ������git stash apply�ָ�������git stash dropɾ����stash������ɾ�����ص������ֳ���
git stash list������Բ鿴�����ֳ���
- **Feature��֧������¹���**
�½���֧����¹��ܡ�
����һ��δ���ϲ����ķ�֧��git branch -D nameǿ��ɾ����
- **����Э��**
����Э������ģʽ:
��git push origin branch-name�����Լ����޸ġ�
��Զ�̷�֧�ȱ��ظ��£����ͻ�ʧ�ܣ�Ҫ����git pull�ϲ����ٴ����͡�
git branch --set-upstream branch-name origin/branch-name   �������ط�֧��Զ�̷�֧�����ӹ�ϵ
git remove -v   �鿴Զ�̿���Ϣ
git checkout -b branch-name origin/branch-name   �������ط�֧��Զ�̷�֧�Ĺ���

��ǩ
---
�ڰ汾���д��ǩ����Ψһȷ�����ǩʱ�̵İ汾��
- git tag name   �����µı�ǩ
- git tag -a tagname -m   ָ����ǩ��Ϣ
- git tag   �鿴���б�ǩ
- git push origin tagname   ����һ�����ر�ǩ��Զ��
- git push origin --tags   ����ȫ��δ���͹��ı��ر�ǩ
- git tag -d tagname   ɾ��һ�����ر�ǩ
- git push origin :refs/tags/tagname   ɾ��һ��Զ�̱�ǩ









