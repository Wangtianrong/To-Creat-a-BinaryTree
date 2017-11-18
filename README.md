# To-Creat-a-BinaryTree
递归创建二叉树，正确做法和错误反思
next CreatBiTree(void) {
	int a;
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
void CreatBiTree(next* T) {
	int a;
	scanf("%d", &a);
	
	if (a < 0) {
		(* T )= NULL;
	}
	else {
		(* T)->data = a;
		t = (next)malloc(sizeof(struct Node));
		CreatBiTree(* (t->left));
		CreatBiTree(* (t->right));
	}
	return ;
}
