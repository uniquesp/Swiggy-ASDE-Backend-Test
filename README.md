# Swiggy-ASDE-Backend-Test Solutions ( 03-07-24 )
## ALL Solutions are Provided in above files

## DSA Quetion
- Extraordinary String
  
# Description
<!-- description:start -->

<p>Each character of the English alphabet has been mapped to a digit as shown below.</p>

<p><img alt="" src="https://fastly.jsdelivr.net/gh/doocs/leetcode@main/solution/2900-2999/2950.Number%20of%20Divisible%20Substrings/images/old_phone_digits.png" style="padding: 10px; width: 200px; height: 200px;" /></p>

<p>A string is <strong>divisible</strong> if the sum of the mapped values of its characters is divisible by its length.</p>

<p>Given a string <code>s</code>, return <em>the number of <strong>divisible substrings</strong> of</em> <code>s</code>.</p>

<p>A <strong>substring</strong> is a contiguous non-empty sequence of characters within a string.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<table border="1" cellspacing="3" style="border-collapse: separate; text-align: center;">
	<tbody>
		<tr>
			<th style="padding: 5px; border: 1px solid black;">Substring</th>
			<th style="padding: 5px; border: 1px solid black;">Mapped</th>
			<th style="padding: 5px; border: 1px solid black;">Sum</th>
			<th style="padding: 5px; border: 1px solid black;">Length</th>
			<th style="padding: 5px; border: 1px solid black;">Divisible?</th>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">a</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">s</td>
			<td style="padding: 5px; border: 1px solid black;">7</td>
			<td style="padding: 5px; border: 1px solid black;">7</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">d</td>
			<td style="padding: 5px; border: 1px solid black;">2</td>
			<td style="padding: 5px; border: 1px solid black;">2</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">f</td>
			<td style="padding: 5px; border: 1px solid black;">3</td>
			<td style="padding: 5px; border: 1px solid black;">3</td>
			<td style="padding: 5px; border: 1px solid black;">1</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">as</td>
			<td style="padding: 5px; border: 1px solid black;">1, 7</td>
			<td style="padding: 5px; border: 1px solid black;">8</td>
			<td style="padding: 5px; border: 1px solid black;">2</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">sd</td>
			<td style="padding: 5px; border: 1px solid black;">7, 2</td>
			<td style="padding: 5px; border: 1px solid black;">9</td>
			<td style="padding: 5px; border: 1px solid black;">2</td>
			<td style="padding: 5px; border: 1px solid black;">No</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">df</td>
			<td style="padding: 5px; border: 1px solid black;">2, 3</td>
			<td style="padding: 5px; border: 1px solid black;">5</td>
			<td style="padding: 5px; border: 1px solid black;">2</td>
			<td style="padding: 5px; border: 1px solid black;">No</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">asd</td>
			<td style="padding: 5px; border: 1px solid black;">1, 7, 2</td>
			<td style="padding: 5px; border: 1px solid black;">10</td>
			<td style="padding: 5px; border: 1px solid black;">3</td>
			<td style="padding: 5px; border: 1px solid black;">No</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">sdf</td>
			<td style="padding: 5px; border: 1px solid black;">7, 2, 3</td>
			<td style="padding: 5px; border: 1px solid black;">12</td>
			<td style="padding: 5px; border: 1px solid black;">3</td>
			<td style="padding: 5px; border: 1px solid black;">Yes</td>
		</tr>
		<tr>
			<td style="padding: 5px; border: 1px solid black;">asdf</td>
			<td style="padding: 5px; border: 1px solid black;">1, 7, 2, 3</td>
			<td style="padding: 5px; border: 1px solid black;">13</td>
			<td style="padding: 5px; border: 1px solid black;">4</td>
			<td style="padding: 5px; border: 1px solid black;">No</td>
		</tr>
	</tbody>
</table>

<pre>
<strong>Input:</strong> word = &quot;asdf&quot;
<strong>Output:</strong> 6
<strong>Explanation:</strong> The table above contains the details about every substring of word, and we can see that 6 of them are divisible.
</pre>

<p><strong class="example">Example 2:</strong></p>

<pre>
<strong>Input:</strong> word = &quot;bdh&quot;
<strong>Output:</strong> 4
<strong>Explanation:</strong> The 4 divisible substrings are: &quot;b&quot;, &quot;d&quot;, &quot;h&quot;, &quot;bdh&quot;.
It can be shown that there are no other substrings of word that are divisible.
</pre>

<p><strong class="example">Example 3:</strong></p>

<pre>
<strong>Input:</strong> word = &quot;abcd&quot;
<strong>Output:</strong> 6
<strong>Explanation:</strong> The 6 divisible substrings are: &quot;a&quot;, &quot;b&quot;, &quot;c&quot;, &quot;d&quot;, &quot;ab&quot;, &quot;cd&quot;.
It can be shown that there are no other substrings of word that are divisible.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= word.length &lt;= 2000</code></li>
	<li><code>word</code> consists only of lowercase English letters.</li>
</ul>
<!-- description:end -->

</hr>

# SQL Question: Binary Tree

[Question Link](https://www.hackerrank.com/challenges/binary-search-tree-1/problem)

### Description
You are given a table, BST, containing two columns: N and P, where N represents the value of a node in a Binary Tree, and P is the parent of N.

Write a query to find the node type of each Binary Tree node ordered by the value of the node. The possible node types are:
- **Root**: If the node is the root of the tree.
- **Leaf**: If the node is a leaf node.
- **Inner**: If the node is neither root nor a leaf node.

### Sample Input
```
 BST Table
 N  |  P
----|----
 1  |  2
 3  |  5
 6  |  8
 8  |  6
 9  |  3
```

### Sample Output
```
1 Leaf
2 Inner
3 Leaf
5 Root
6 Leaf
8 Inner
9 Leaf
```

### Explanation
The Binary Tree below illustrates the sample input:

![Binary Tree](https://s3.amazonaws.com/hr-assets/0/1532493154-b45f2a6d3a-Binary_Tree.png)

- **Root**: Node with value 5.
- **Inner**: Nodes with values 2 and 8.
- **Leaf**: Nodes with values 1, 3, 6, and 9.
  
Refer to the [problem statement](https://www.hackerrank.com/challenges/binary-search-tree-1/problem) for more details and constraints.

</hr>

# REST API Question: Discounted Price

## Description
REST API: Discounted Price

Given a barcode, query the API at `https://jsonmock.hackerrank.com/api/inventory?barcode={barcode}` and return the item's discounted price.

The response is a JSON object with 5 fields. The essential field is `data`.

In the `data` array, the item has the following schema:

- **barcode**: the barcode for the product (String)
- **price**: the gross selling price (Number)
- **discount**: the discount percent to apply (Number)

Fields such as `page`, `per_page`, `total`, `total_pages`, etc., are not required for this task.

If the barcode is found, the `data` array contains exactly 1 element. If not, it is empty and the function should return -1.

An example of the product record from `https://jsonmock.hackerrank.com/api/inventory?barcode=74001755` is:

```json
{
    "barcode": "74001755",
    "item": "Ball Gown",
    "category": "Full Body Outfits",
    "price": 785,
    "discount": 7,
    "available": 1
}
```
</hr>

## ALL THE BEST 
