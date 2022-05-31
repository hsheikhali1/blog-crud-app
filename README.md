# LEARNING CRUD

## What is CRUD
- Create
- Read
- Update
- Delete

### CRUD Application (BACKEND)
A blog CRUD Application

- CREATE
  * Creating the blog post
  * Creating a new user
  * Comments (replies to comments)
  
  example for creating a user
  ```js
  // you've imported some packages to handle database
  
  function createUse(username, email, password) {
	  if (db.findUser(username)) {
		return; // end execution because the user already exists
	  }
	  
	  // we are creating a user!
	  db.create(username, email, password);
  }
  ```

  Creating a blog post
  ```js
  function createPost(postDate, postTitle, description, author, body) {
	  const postsByAuthor = db.findPostByAuthor(author);
	  
	  if (postsByAuthor.find((title) postTitle == title)) {
		return; // end execution
	  }

	  // creating a post
	  db.create(postDate, postTitle, description, author, body);
  }
  ```

- READ (GET)
  * Get posts /api/posts/12345678 -> return post with id 12345678
	* Get a post by author
	* Get a post by id
	* Get posts with a specific date range (Jan 1 - May 30)
	* Get post by title
  * Get Users (All the peeps who registered for your blog)
  * Get all the comments
	* Get comments by author
	* Get comments by id
	* Get comments by date

- UPDATE
  * Edit Posts
  * Edit Comments
  * Edit Profile
  
  ```js
  function updatePost(postId, updatePostBody) {
	  db.updatePost(postId, updatePostBody);
  }
  ```
  
  ```js

  function updateComment(commentId, updateCommentBody) {
	  db.updateComment(commentId, updateCommentBody);
  }
  ```
	
- DELETE
  * Delete Post
  * Delete Comment
  * Delete Profile

  ```js
  function deletePost(postId) {
	  db.deletePost(postId);
  }
  ```
  
  ```js
  function deleteComment(commentId) {
	  db.deleteComment(commentId);
  }
  ```


### CRUD Application (FRONTEND)
Blog Application frontend
