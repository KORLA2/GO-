
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
   func min_in_right_sub_tree(root *node) int {
    	min := 0
    	for root != nil {
    		min = root.val
    		root = root.left
    
    	}
    	return min
    }
```
```
     func find(root *node, val int) *node {
    
    	if root == nil || root.val == val {
    		return root
    	}
    	if val < root.val {
    		return find(root.left, val)
    	} else {
    		return find(root.right, val)
    	}
    
    }
```
```
  func inorder_successor(root *node, val int) int {
  
  	var current *node = find(root, val)
  
  	if current.right != nil {
  		return min_in_right_sub_tree(current.right)
  	} else {
  		successor := 0
  		ancestor := root
  		for ancestor != current {
  			if ancestor.val < current.val {
  				ancestor = ancestor.right
  			} else {
  				successor = ancestor.val
  				ancestor = ancestor.left
  			}
  
  		}
  		return successor
  	}
  
  }

```
    func main(){
  /*
          14
        /    \ 
       10    20
      /  \   / \
     5   12 15 25 
  
  */
  
  fmt.Print(inorder_successor(root , val ))
  }

```
