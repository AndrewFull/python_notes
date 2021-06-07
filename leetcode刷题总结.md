# 1.链表

###反转链表

```python
def reverse(head):
    if not head: return None
    last = None
    p = head
    while p:
        tmp = p.next
        p.next = last
        last = p
        p = tmp
    return last
```

###链表中点：快慢指针

```python
def middle(head):
    if not head: return None
    s = f = head
    while f.next and f.next.next:
        s = s.next
        f = f.next.next
    return s
```

###链表交点：双指针

```python
def cross(head1,head2):
  	h1, h2 = head1, head2
  	while h1!=h2:
      	h1 = head2 if not h1 else h1.next
        h2 = head1 if not h2 else h2.next
    return h1
```

###链表合并

# 2.区间合并



#3.采样

## 1.蓄水池采样

目的：针对大量数据进行随机采样，无法一次被内存读取的情况。一次遍历数据即可得到结果。



