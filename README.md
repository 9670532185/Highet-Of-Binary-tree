# Highet-Of-Binary-tree


public class BinaryExamNode <T>{
    T data;
    BinaryExamNode<T> left;
    BinaryExamNode<T> Right;
    BinaryExamNode(T data)
    {
        this.data=data;

    }

public static int Highet(BinaryExamNode<Integer> root)
{
    if(root==null)
    {
        return 0;
    }
    int LeftHi=Highet(root.left);
    int RightHi=Highet(root.Right);
    int myhighet= Math.max(LeftHi,RightHi)+1;
    return myhighet;
}
    
    public static void main(String[] args)
    {
BinaryExamNode<Integer> root=new BinaryExamNode<Integer>(1);
BinaryExamNode<Integer> rootLeft=new BinaryExamNode<Integer>(2);
BinaryExamNode<Integer> rootRight=new BinaryExamNode<Integer>(3);
root.left=rootLeft;
root.Right=rootRight;
System.out.println(Highet(root));

    }
}
