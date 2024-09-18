https://leetcode.com/problem-list/e97a9e5m/

SELECT name, COALESCE(SUM(distance),0) AS travelled_distance
FROM Users LEFT JOIN Rides ON Users.id = Rides.user_id GROUP BY Users.id ORDER BY SUM(distance) DESC, name ASC;

Ghi chu: 2 van de can luu y:
1) Co the co nhieu user trung ten => GROUP BY Users.id
2) SUM(NULL) thanh NULL nen phai dung COALESCE
