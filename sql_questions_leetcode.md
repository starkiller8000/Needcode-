https://leetcode.com/problem-list/e97a9e5m/

SELECT name, COALESCE(SUM(distance),0) AS travelled_distance
FROM Users LEFT JOIN Rides ON Users.id = Rides.user_id GROUP BY name ORDER BY SUM(distance) DESC, name ASC;
