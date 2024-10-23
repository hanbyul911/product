# products
<상품>
|기능|매서드|URI|method|view|redirect URI|
|--------|-----|-----|-----|------|-------|
|상품 목록 조회|get|/products?action=list|list()|productList.jsp|
|상품 등록|get|/products?action=insert|insert()|productInsert.jsp|
|            |post|/products?action=insert|insert()|productInsert.jsp|/products?action=list|
|상품 상세 조회|get|/products?action=info&id=1|info()|productInfo.jsp|
|상품 수정|get|/products?action=update&id=1|update()|productUpdate.jsp|   
|            |post|/products?action=update&id=1|update()|productUpdate.jsp|/products?action=info&id=1|
|상품 삭제|post|/products?action=delete&id=1|delete()|productList.jsp|/products?action=list|


# DB
<product>
    
|id|name|category|price|quantity|description|
|--|----|--------|-----|-------|------------|
|1|종이컵|생활용품|1000|10|물 맛이 좋아지는 종이컵|
|2|hdmi 연결선|전자제품|10480|100|당신의 눈을 안녕하게 해줄 투모니터를 위한 최적품|
    
<db 생성 sql>

```sql
create table product (
    id int primary key auto_increment,
    name varchar(100) not null,
    price int not null,
    quantity int default 0,
    category varchar(50),
    description varchar(255)
)
```
