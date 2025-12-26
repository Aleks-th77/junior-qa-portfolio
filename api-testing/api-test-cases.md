# API Test Cases — JSONPlaceholder

### TC-API-01 Get list of posts
**Method:** GET  
**Endpoint:** /posts  

**Steps:**
1. Send GET request to /posts

**Expected result:**
- Status code 200
- Response body contains a list of posts

---

### TC-API-02 Get post by ID
**Method:** GET  
**Endpoint:** /posts/1  

**Steps:**
1. Send GET request to /posts/1

**Expected result:**
- Status code 200
- Response contains post with id = 1

---

### TC-API-03 Create new post
**Method:** POST  
**Endpoint:** /posts  

**Body:**
```json
{
  "title": "test",
  "body": "api testing",
  "userId": 1
}
