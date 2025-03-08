```
  package main;
  import "fmt"

```
```
   type node struct {
   val int
   left* node
   right*node
  
  }

```


```
    func checkBST(root*node,min int,max int) bool{
    
    if root==nil { return true;}
    
   /*
     if root.val<min || root.val>max{
      return false;
    }
   */
    return root.val>min&&root.val<max&&checkBST(root.left,min,root.val)&&checkBST(root.right,root.val,max)  

}
  

```

```
    func main(){
  /*
          14
        /    \ 
       10    20
      /  \   / \
     5   12 15 25 
  
  */
  
  fmt.Print(checkBST(root,math.MinInt32,math.MaxInt32))
  }

```
