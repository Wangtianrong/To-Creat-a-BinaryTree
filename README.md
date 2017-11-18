# To-Creat-a-BinaryTree
递归创建二叉树，正确做法和错误反思
next CreatBiTree(void) {
	char a;
	scanf("%d", &a);
	next t = (next)malloc(sizeof(struct Node));
	if (a < 0) {
		t = NULL;
	}
	else {
		t->data = a;
		t->left = CreatBiTree();
		t->right = CreatBiTree();
	}
	return t;
}
//正确做法
void CreatBiTree(next T) {
	char a;
	scanf("%d", &a);
	
	if (a < 0) {
		T = NULL;
	}
	else {
		T = (next)malloc(sizeof(struct Node));
		T->data = a;
		CreatBiTree(t->left);
		CreatBiTree(t->right);
	}
	return ;
}
