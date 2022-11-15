# 합계 함수

1. ROLLUP

GROUP BY로 묶은 각각의 소그룹 합계와 전체 합계

```
SELECT 상품ID, 월, SUM(매출액) AS 매출액
FROM 월별매출
GROUP BY ROLLUP(상품ID, 월);
```

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>





