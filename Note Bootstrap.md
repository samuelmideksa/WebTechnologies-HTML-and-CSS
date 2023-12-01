# Bootstrap

Course: Web Technologies (https://www.notion.so/Web-Technologies-9040d79d92844804bec7c112fc8e43e6?pvs=21)
Next Review: November 25, 2023
Materials: https://getbootstrap.com/, https://www.tutorialrepublic.com/
Note type: Lecture Note
Lecture day: November 25, 2023

- Breakpoints
    
    Breakpoints are customizable widths that determine how your responsive layout behaves across device or viewport sizes in Bootstrap.
    
    ## **Available breakpoints**
    
    Bootstrap includes six default breakpoints, sometimes referred to as *grid tiers*, for building responsively. These breakpoints can be customized if you’re using our source Sass files.
    
    | Breakpoint | Class infix | Dimensions |
    | --- | --- | --- |
    | Extra small | None | <576px |
    | Small | sm | ≥576px |
    | Medium | md | ≥768px |
    | Large | lg | ≥992px |
    | Extra large | xl | ≥1200px |
    | Extra extra large | xxl | ≥1400px |

- Containers
    
    Containers are the most basic layout element in Bootstrap and are **required when using our default grid system**. Containers are used to contain, pad, and (sometimes) center the content within them.
    
    - `.container`, which sets a `max-width` at each responsive breakpoint
        
        # **Creating Responsive Fixed-width Containers**
        
        You can simply use the `.container` class to create a responsive, fixed-width container. The width of the container will change at different breakpoints or screen sizes, as shown above.
        
        ****Example[Try this code »](https://www.tutorialrepublic.com/codelab.php?topic=bootstrap&file=responsive-fixed-width-container)**
        
        ```markup
        <div class="container"><h1>This is a heading</h1><p>This is a paragraph of text.</p></div>
        ```
        
    - `.container-{breakpoint}`, which is `width: 100%` until the specified breakpoint
        
        # **Specify Responsive Breakpoints for Containers**
        
        Since Bootstrap v4.4, you can also create containers that is 100% wide until the specified breakpoint is reached, after which max-width for each of the higher breakpoints will be applied.
        
        | Bootstrap  Grid System | X-Small<576px | Small≥576px | Medium≥768px | Large≥992px | X-Large≥1200px | XX-Large≥1400px |
        | --- | --- | --- | --- | --- | --- | --- |
        | .container | 100% | 540px | 720px | 960px | 1140px | 1320px |
        | .container-sm | 100% | 540px | 720px | 960px | 1140px | 1320px |
        | .container-md | 100% | 100% | 720px | 960px | 1140px | 1320px |
        | .container-lg | 100% | 100% | 100% | 960px | 1140px | 1320px |
        | .container-xl | 100% | 100% | 100% | 100% | 1140px | 1320px |
        | .container-xxl | 100% | 100% | 100% | 100% | 100% | 1320px |
        | .container-fluid | 100% | 100% | 100% | 100% | 100% | 100% |
        
        For example, `.container-xl` will be 100% wide until the xl breakpoint is reached (i.e., viewport width ≥ 1200px), after which max-width for xl breakpoint is applied, which is 1140px.
        
        ****Example[Try this code »](https://www.tutorialrepublic.com/codelab.php?topic=bootstrap&file=specify-responsive-breakpoints-for-containers)**
        
        ```markup
        <div class="container-sm">100% wide until screen size less than 576px</div><div class="container-md">100% wide until screen size less than 768px</div><div class="container-lg">100% wide until screen size less than 992px</div><div class="container-xl">100% wide until screen size less than 1200px</div>
        ```
        
    - `.container-fluid`, which is `width: 100%` at all breakpoints
        
        # **Creating Fluid Containers**
        
        You can use the `.container-fluid` class to create a full width container. The width of the fluid container will always be 100% irrespective of the devices or screen sizes.
        
        ****Example[Try this code »](https://www.tutorialrepublic.com/codelab.php?topic=bootstrap&file=fluid-container)**
        
        ```markup
        <div class="container-fluid"><h1>This is a heading</h1><p>This is a paragraph of text.</p></div>
        ```
        

- **Grid system**
    
    Use our powerful mobile-first flexbox grid to build layouts of all shapes and sizes thanks to a twelve column system, six default responsive tiers, Sass variables and mixins, and dozens of predefined classes.
    

- Card
    
    A **card** is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options. If you’re familiar with Bootstrap 3, cards replace our old panels, wells, and thumbnails. Similar functionality to those components is available as modifier classes for cards.
    
    ```html
    <div class="card" style="width: 18rem;">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
    </div>
    ```
    

- ****Bootstrap Grid System****
    
    Bootstrap grid system provides an easy and powerful way to create responsive layouts of all shapes and sizes. It is built with [flexbox](https://www.tutorialrepublic.com/css-tutorial/css3-flexible-box-layouts.php) with mobile-first approach. Also, it is fully responsive and uses twelve column system (12 columns available per row) and six default responsive tiers.
    

- **Creating Column Layouts**
    
    The following example will show you how to create two column layouts for medium, large and extra large devices like tables, laptops and desktops etc. However, on mobile phones (screen width less than 768px), the columns will automatically become horizontal (2 rows, 1 column).
    
    ```html
    <div class="container">
        <!--Row with two equal columns-->
        <div class="row">
            <div class="col-md-6">Column left</div>
            <div class="col-md-6">Column right</div>
        </div>
        
        <!--Row with two columns divided in 1:2 ratio-->
        <div class="row">
            <div class="col-md-4">Column left</div>
            <div class="col-md-8">Column right</div>
        </div>
        
        <!--Row with two columns divided in 1:3 ratio-->
        <div class="row">
            <div class="col-md-3">Column left</div>
            <div class="col-md-9">Column right</div>
        </div>
    </div>
    ```