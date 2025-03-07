```
package main

import "fmt"

type node struct {
	val   int
	left  *node
	right *node
}

func insert(root *node, val int) *node {

	if root == nil {
		return &node{val, nil, nil}
	} else if val < root.val {
		root.left = insert(root.left, val)
	} else {
		root.right = insert(root.right, val)
	}
	return root

}

func traverse(root *node) {

	//level order traversal
	var q = []*node{}

	q = append(q, root)
	level := 1
	for len(q) > 0 {

		front := q[0]
		q = q[1:]
		fmt.Print(front.val, " ")
		if front.left != nil {
			q = append(q, front.left)
		}
		if front.right != nil {
			q = append(q, front.right)
		}

		level--

		if level == 0 {
			level = len(q)
			fmt.Println()
		}
	}
}

func max_in_left_sub_tree(root *node) *node {

	if root.right == nil && root.left == nil {
		return root
	}

	return max_in_left_sub_tree(root.right)

}

   //   14
	//    / \
	//   12   15
	//  / \
	// 8   13
 // / \
 //2  10 

func delete(root *node, val int) *node {

	if root == nil {
		return nil

	}

	if val < root.val {
		root.left = delete(root.left, val)

	} else if val > root.val {
		root.right = delete(root.right, val)
	} else {

		if root.left == nil && root.right == nil {

			return nil
		} else if root.left != nil && root.right != nil {

			proot := max_in_left_sub_tree(root.left)

			root.val = proot.val
			root.left = delete(root.left, proot.val)
			return root
		} else if root.left == nil {
			temp := root.right
			root.right = nil
			return temp

		} else if root.right == nil {

			temp := root.left
			root.left = nil
			return temp
		}

	}

	return root

}

func main() {
	var root *node = &node{14, nil, nil}

	insert(root, 12)
	insert(root, 15)
	insert(root, 13)
	insert(root, 8)
	insert(root, 2)
	insert(root, 10)

	// fmt.Println(root.val)
	delete(root, 14)

	traverse(root)

	//     14
	//    / \
	//   12   15
	//  / \
	// 8   13
 // / \
 //2  10  
 
	// delete(root, 2)

}
```
