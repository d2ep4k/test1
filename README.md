# test1
## functional requirements 
- multiple users can create/delete/modify account
- user can login using google or other accounts
- user can post blog
- user can modify posted blog
- user can share their comment on the blog
- user can reply to a comment
- user can add images to their blog
---
*secondary*
- blog may include latex, video, audio
- user can follow other users (publish - subscriber model)
- blog recommendations
- plagiarism check
- automated reply


##  UI view design
![WhatsApp Image 2023-12-15 at 5 02 51 PM](https://github.com/d2ep4k/test1/assets/143197927/6b4bcbd4-42c1-4554-92cd-e984dbedcd66)

![WhatsApp Image 2023-12-15 at 5 24 40 PM](https://github.com/d2ep4k/test1/assets/143197927/0eb76e6f-55cb-4723-9352-5e241a7b09d6)

## database LLD
```
class user{
    int userId;
    string userName;
    string emailId;
    string password;
    vector<int> followers, following;   //stores userId 
    vector<int> posts;  //stores postId
    
};

class reply{
    int replyId;
    int likes;
    string text;
};

class comment{
    int commentId;
    int likes;
    string text;
    vector<int> replies;
};

class post{
    int postId;
    int owner;  //stores userId
    int views, likes;
    vector<int> comments;   // store commentId
    string createdAt, lastModified;    //stores date-time
    string title, content;      //body of blog, json better alternative
    vector<blob> images;
};
```
