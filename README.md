# Top Data Structure Interview Questions In Swift
Here is the list of top data structure questions asked in interviews

## Topics

### Linked List
1. **Linked List Cycle Detection**
> Given the head of a linked list, determine if the linked list has a cycle in it.
There is a cycle in a linked list if there is some node in the list that can be reached again by continuously following the next pointer. Internally, pos is used to denote the index of the node that the tail's next pointer is connected to. Note that pos is not passed as a parameter.

```
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     public var val: Int
 *     public var next: ListNode?
 *     public init(_ val: Int) {
 *         self.val = val
 *         self.next = nil
 *     }
 * }
 */

class Solution {
    func hasCycle(_ head: ListNode?) -> Bool {
        
        var sl = head
        var fast = head?.next?.next
        while (fast != nil) {
            if (sl === fast) {
                return true
            }
            sl = sl?.next
            fast = fast?.next?.next
        }

        return false
    }
}
```
