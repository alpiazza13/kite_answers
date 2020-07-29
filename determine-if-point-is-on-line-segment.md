headers:
    use-point-slope: Use point slope
---
# How to determine if a point is on a line segment in Python
A line segment can be defined by two points `pt1` and `pt2`, each with an x and y coordinate. If `pt1 = (0,0)` and `pt2 = (5,5)`, the point `(2,2)` is on the line.



## Use the point slope formula to check if the point is on the line segment {#use-point-slope}
Define `pt1` and `pt2` as tuples representing the two points of the line segment, and `pt3` as the point in question. `x1, x2, x3` and `y1, y2, y3` represent the x and y coordinates of the 3 points. Use the point slope formula to determine the slope, `m`, of the line. Use the same formula to determine if `pt3` lies on the line. Then, since the line is really a line segment, calculate if `pt3` is between `pt1` and `pt2`. If both of these are true, the point in question lies on the line segment.
```python
pt1 = (0,0)
pt2 = (5,5)
pt3 = (2,2)
x1, x2, x3 = pt1[0], pt2[0], pt3[0]
y1, y2, y3 = pt1[1], pt2[1], pt3[1]
m = (y2 - y1) / (x2 - x1)
pt3_on = (y3 - y1) == m * (x3 - x1)
pt3_between = (min(x1, x2) <= x3 <= max(x1, x2)) and (min(y1, y2) <= y3 <= max(y1, y2))
on_and_between = pt3_on and pt3_between
print(on_and_between)
```

If the x-coordinates of the start and end points of the line are the same, the slope of the line will be undefined, so a different solution is required. In this case, simply check if `x3 == x2` and if `y3` lies between `y1` and `y2`. Note that `pt1` must be defined as the "bottom" point of the vertical line (`y1` must be less than or equal to `y3`) to avoid using `min` and `max` again.
```python
pt1 = (0,0)
pt2 = (0,5)
pt3 = (0,3)
x1, x2, x3 = pt1[0], pt2[0], pt3[0]
y1, y2, y3 = pt1[1], pt2[1], pt3[1]
on_and_between = (x3 == x2) and (y1 <= y3 <= y2)
print(on_and_between)
```
> **Further reading:**
> The point slope formula is used for many algebraic calculations. You can read more about it [here](https://www.mathsisfun.com/algebra/line-equation-point-slope.html).
