package main

import (
	"fmt"
	"slices"
)

func main() {

	slice := make([]int, 7)
	slice[0] = 8
	slice[1] = 18
	slice[2] = 81
	slice[3] = 28

	plice := slices.Clone(slice) // Assign slice to plice in a way that changing one wouldn't effect other
	plice[0] = 89

	slices.Sort(slice) // Sorting in ascending order

   // Sorting in ascending order
	slices.SortFunc(slice, func(x, y int) int {
		if x < y {
			return 1
		} else if x > y {
			return -1
		}
		return 0
	})
	fmt.Println(slice)

}
