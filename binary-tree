class Node {
    int value;
    Node left;
    Node right;
    
    Node(int value) {
        this.value = value;
        left = null;
        right = null;
    }
}

class BinaryTree {
    
    //Create Binary Tree through recursion
    public Node insert(Node current, int value)
    {
        if(current == null) {
            return new Node(value);
        }
        
        if(current.value > value) {
            current.left = insert(current.left, value);
        } else if(current.value < value) {
            current.right = insert(current.right, value);
        } 
        
        return current;
    }
    
    //Inorder traversal
    // Left, Root, Right
    public void inorder(Node root) {
        if(root == null) {
            return;
        }
        
        inorder(root.left);
        System.out.print(root.value + " ");
        inorder(root.right);
    }
    
     //Preorder traversal
    // Root, Left, Right
     public void preorder(Node root) {
        if(root == null) {
            return;
        }
        
        System.out.print( root.value + " ");
        preorder(root.left);
        preorder(root.right);
    }
    
      //Postorder traversal
     // Left,Right, Root
     public void postorder(Node root) {
        if(root == null) {
            return;
        }
        
        postorder(root.left);
        postorder(root.right);
        System.out.print(root.value + " ");
    }
    
    public Node search(Node root, int value) {
        if(root == null) {
            return null;
        }
        else if(root.value == value) {
            return root;
        } else if(root.value > value) {
            return search(root.left, value);
        } else {
            return search(root.right, value);
        }
    }
}

class HelloWorld {
    public static void main(String[] args) {
        BinaryTree bt = new BinaryTree();
        Node root = null;
        root = bt.insert(root, 6);
        root = bt.insert(root, 3);
        root = bt.insert(root, 4);
        root = bt.insert(root, 1);
        root = bt.insert(root, 9);
        root = bt.insert(root, 5);
        root = bt.insert(root, 11);
        
        System.out.println("In Order Traversal");
        bt.inorder(root);
        System.out.println("Pre Order Traversal");
        bt.preorder(root);
        System.out.println("Post Order Traversal");
        bt.postorder(root);
        
        System.out.println("Element Available: " + bt.search(root, 9));
    }
}
