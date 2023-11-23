# HTML Tags

Course: Web Technologies (https://www.notion.so/Web-Technologies-9040d79d92844804bec7c112fc8e43e6?pvs=21)
Date: November 25, 2023
Type: Assignment
Status: In Progress

15 HTML Tags

- Embed: to embed external resources to our page
    
    ```html
    <embed type="video/webm" src="blabla.youtube.com">
    ```
    
- Script: to define a client side script
    
    ```html
    <script> <!-- Script goes here --> </script>
    <script src="script.js"></script>
    ```
    
- div: to group sections of a webpage together
    
    ```html
    <div id="navigation">
    	<ul>
    		<li> Home </li>
    		<li> login </li>
    		<li> conact </li>
    	</ul>
    </div>
    ```
    
- image
    
    ![Untitled](HTML%20Tags%207b4b046692ed4108846b0ac2be62d9e3/Untitled.png)
    
- List
    - ordered list: list with numbering (could be lettered)
        
        ```html
        <ol>
        	<li> coffee </li>
        	<li> tea </li>
        	<li> macchiato </li>
        </ol>
        ```
        
    - unordered list
        
        ```html
        <ol>
        	<li> coffee </li>
        	<li> tea </li>
        	<li> macchiato </li>
        </ol>
        ```
        
- template: Defines a container for content that should be hidden when the page loads
    
    ```html
    <template>
      <h2>Flower</h2>
      <img src="img_white_flower.jpg" width="214" height="204">
    </template>
    ```
    
- iframe: to embed another document within the current HTML document.
    
    ```html
    <iframe src="demo_iframe.htm" style="height:200px;width:300px;" title="Iframe Example"></iframe>
    ```
    
- anchor: to link
    
    ```html
    <a href="www.html.com">
    ```
    
- video
    
    ```html
    <video width="320" height="240" controls>
      <source src="movie.mp4" type="video/mp4">
      <source src="movie.ogg" type="video/ogg">
    Your browser does not support the video tag.
    </video>
    ```
    
- `<table>`: to create a table structure
    
    ```html
    <table>
      <tr>
        <th>First Name</th>
        <th>Last Name</th>
      </tr>
      <tr>
        <td>John</td>
        <td>Doe</td>
      </tr>
      <tr>
        <td>Jane</td>
        <td>Smith</td>
      </tr>
    </table>
    
    ```
    
- `<form>`: to create a form for user input
    
    ```html
    <form action="/submit" method="post">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name">
    
      <label for="email">Email:</label>
      <input type="email" id="email" name="email">
    
      <input type="submit" value="Submit">
    </form>
    
    ```
    
- `<h1>` to `<h6>`: to define headings with different levels of importance
    
    ```html
    <h1>This is Heading 1</h1>
    <h2>This is Heading 2</h2>
    <h3>This is Heading 3</h3>
    
    ```
    
- `<span>`: to apply styles or manipulate specific portions of text
    
    ```html
    <p>My favorite color is <span style="color: blue;">blue</span>.</p>
    
    ```
    
- `<button>`: to create a clickable button
    
    ```html
    <button type="button">Click Me</button>
    
    ```