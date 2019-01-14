


### Terminal

    -touch (fileName.ext) ---- to create new file
    -rm is to remove/delete
    -rm -rf will delete folder

### Git
    -git add <filename>
    -git commit -m 'Message'
    -git init, git status, red it not in staging, green is
    -git add . ---- all files go into staging area
    -if you get stuck in vin do :q


### Github
    -git hub is an online resource to save your code
    Flow up
    -Githup
    -git
    -computer

    -




### Functions
    -

### Arrays
    -for(var i =0; i<3; i++) 
        -first -- where in array loop starts
        -second -- checks fo logic
        -third -- runs logic {}
        -fourth -- increments the value of i to loop again until value of i does not meet requirements of step 2
    -.push adds to the end of the array
    -.unshift adds to the beginning of the array
    -.pop removes from the end of the array
    -.shift removes from the beginning of the array
    -.splice is used to remove items from array (where to start in array,how many items to remove) used to add items in (where to start,0 items to remove,'element to insert')
    -.slice used to get copies of an entire array or just peices of it (start at index, what index to stop at) does not modify the array, coppies to get elements out
    -
    -How to make a string numbers only using parseInt()
                            var beeSting = [1,'2',4]
                            function notAString(arr){
                                newArr = [];
                                for( var i = 0; i < arr.length; i++){
                                newArr.push(parseInt(arr[i]))
                                }
                               return newArr;
                            }
                            notAString(beeSting)
                          
    -.indexOf() -- if the search is not in array indexOf will return -1, if search is in array itll return the index of the searched Item
    -.forEach -- go through each item 1 at a time and pass it through a function we give it. -- does not return a value
    -.map works just like a .forEach but returns a value in a new empty array
    -.filter -- filters array through criteria -- 
                                var names = ['suzie', 'Ben', 'mark', 'frankline]
                                var shortNames = names.filter(function(val,i,arr){
                                    return val.length < 5;
                                })
                                shortNames = ['ben', 'mark']
                                names = ['suzie', 'Ben', 'mark', 'frankline]
    -






Objects
    -Example for how to change a object within a function
            -var user = {
                name: 'Sally Rally',
                pwHash: 'U+Ldlngx2BYQk',
                username: 'SallyRally801'
            };

            function personalize(obj) {
            for(var key in user){
                user.name='Ryan',
                user.pwHash='43df90w_h',
                user.username='ryanleeeallred';
            }
            return user;
            }
    -Delete -- delete is a keyword -- delete myObj.property
                var backpack = {
                    oldLaptop: 'slow',
                    oldLunch: 'moldy',
                    pencil:'sharp,
                }
                var oldStuff = ['oldLaptop', 'oldLunch']
                for (var i = 0; i<oldStuff.length; i++){
                    delete backpack [oldStuff[i];]
                }

    -copying with an assign
                -newObj = Object.assign({},obj) (capital 'O' in Object.assign)
    - for in loops
                for(var variable in obj){
                    console.log(obj[variable])
                }
    

callback
    -setTimeout(function,time in milliseconds delayed) 
    -


    
    
    
### CSS & HTML
    
#### CSS
    -CSS specifity (Specifif (starting with most))
        -Inline styling(1000)
        -id(100)
        -class, pseudo-class(10)
        -element(1)
        -DRY(DO NOT REPEAT YOURSELF)
        -consolidate your tags -- i.e
        -Do not
            -.post1 {info}
            -.post1 h2 {info}
            -.post2 {same info as post1}
            -.post2 h2{same as post1 h2}
        -Do
            -.post {info}
            -.post h2 {info}
        -use classes to style many elemenets
        -style as generally as you can, then make any adjustments 
        to more specific selections
        -semantic HTML can help you name elements more intuitively 
        and have fewer classs overlaps
    -Reset CSS
        -reset.css or normalize.css
        -reset.css
        -removes built in default browser styles
        -normalize.css
        -helps have more consistant style across broswers
    -META tags
        -located normaly in the <head></head>
        -name='description' content ='description of website'
        -name='keywords' content = 'ha,lol,no'
        -name='author' content= 'author'
        -name ='viewport' conten='scale'
    -Display Property
        -display:inline -- make divs from columns to row, elements 
        do not get their own height or width, they share those properties
        -display:inline-block -- modify individual properties
        -default is (display:block) there by default no need to add -- divs in columns
        -Text Properties
        -font-size -- em(basesize),px(pixels),vh(percent of viewer height)
        -color -- color to text
        -line-height:em,px
        -background color -- highlight
        -text-alighnment -- right, center, left
        -font-family -- font style
        -letter spacing -- em,px
    
        -Apply through normal CSS styling editors
        -headers
        -Background Properties
        -background-image -- :url('string to path for image'), relative path to something 
        local on computer or online link
        -background-position -- top center, cover
        -background-size --
        -background
        -background-color -- color for background
        -Width and Height
        -number px;
        -view height/width -- percent of viewer screen.

    -Beth HTML & CSS Lecture
                -


### REACT
                -Components
                    -Always capitalize react components -- html is lower case so it makes it easier for program to know when component is threre.
                    -can use components to use other components
                -JSX 
                    -to evaluate using javascript 
                        var variableName = 'Love Ryan'
                        text={variableName}
                    
                -Terms
                    -text='write here'
                    -
                -Import and Export
                    -Import
                        -Import at top
                    -Export
                        -Export at the bottom
                
                -State
                    -Can have state or no state depending on if we want them to
                    -two components will not share data but will stay private
                    -use state for data that changes in a component
                    -set state in constructor function
                    -
                    -   -this.state = {
                        things you want to keep track of
                    -state is a way of passing data
                        -used to keep track of changing data in a component
                    -
                    }
                -Prop
                    -Dont change probs but display the data in props
                    -if our component needs to keep track of data it would be state, if it something that needs to be data passed down from a parent component thats a prop
                    -
                -React-Router
                    -import {HashRouter as Router, Route, Switch} from 'react-router-dom';
                        <Router>
                         <Switch>
                            <Route exact path='/' component={Home}/>            Use exact for the home page and use switch if you want only 1 active
                            <Route path='/about' component={About}/>
                            <Rout path='/store' render={()=> (
                                <Store>
                                    <Switch>
                                        <Route component={StoreLanding}
                                        <Route path='/store/nails' component={Nails}
                                        <Route path='/store/drills' component={Drills}
                                        <Route path='/store/hammers' component={Hammers} 
                                    </Switch>
                                </Store>
                                )}/>
                         </Switch>
                        </Router>

                        Routes.md Notes
                            -Route/Home
                            -Route /about About
                            -Route /store Store
                                -Store
                                -Route /store/nails nails
                                -Route /store/hammers hammers
                                -Route /store/drills drills
                            
### SQL 
        -The Concept
            -Relational Databases are like giant excel spreadsheets
            -modern databases have millions/billions of individual data on a single table
            -Applications that are really good at storing big tables and communicate very fast
            
        -Primary Keys
            -Another column with an Id that only 1 person will have assigned
            -key assigned to identify each row: Must be unique and Constant
            
        -Schemas
            -columns
                -id
                -student_name
                -grade
                -teacher_id
            -type
                -INT
                -VARCHAR(60)
                -DECIMAL
                -INT
            -Modifiers
                -Primary Key
                -Auto Increment
                -References Teachers(id)

        -Select Statements
            -Queary 
            -Select*From Cites;
                -Select(Search)
                -*(All Columns)
                -From(What table you want to choose from)
                -Cities(name of example table)
            -SELECT [column] FROM [table]

        -WHERE Keyword for Conditional Selects
            -WHERE [Criteria]
                -'=','>=','>','<','!='
                -Uses 'AND','OR' as well as posible Criteria
                -Using 'LIKE' is not casesensitive by default
                -Where Statements are CaseSensitive by default
                -=Null wont work but IS NULL Will
                -'BETWEEN' Is just a shortcut 
                - IN(Value) NOT IN(value)
        -Adding, Updating, Removing
            -Adding
                -INSERT INTO [Table Name] (valueColumn,valueColumn2)
                                -VALUES(info, info2)
            -Updating
                -UPDATE [Table Name]
                    SET[columnName] = 'example'
                    WHERE id = [id]
            -Delete
                -DELETE FROM [table]
                    WHERE [table] [operator] [Number]

        -InClass Practice
                     DROP TABLE IF EXISTS account;

                    CREATE TABLE account
                    (
                    -- id serial primary key
                        id integer PRIMARY KEY autoincrement,
                        name VARCHAR(25) NOT NULL,
                        email text
                    );

                    insert into account
                        (name, email)
                    values
                        ('Kenn', 'klambshine0@quantcast.com');
                        -SQL-1-Afternoon
                                                                                    /*create TABLE person 
                                                            (
                                                            person_id integer primary key autoincrement,
                                                            Name text not null,
                                                            Age integer not null,
                                                            Height integer not null,
                                                            City text not null,
                                                            Favorite_color text not null
                                                            )*/
                                                            
                                                            /*	insert into person (Name, Age, Height, City, Favorite_Color)
                                                            values ('Ryan', 20,  140, 'Seattle', 'Green');
                                                            
                                                                insert into person (Name, Age, Height, City, Favorite_Color)
                                                            values ('Michael', 28,  148, 'Seattle', 'Red');
                                                            
                                                                insert into person (Name, Age, Height, City, Favorite_Color)
                                                            values ('Brittany', 30,  120, 'Seattle', 'Teal');
                                                            
                                                                insert into person (Name, Age, Height, City, Favorite_Color)
                                                            values ('Tanner', 16,  138, 'Seattle', 'Blue');
                                                            
                                                                insert into person (Name, Age, Height, City, Favorite_Color)
                                                            values ('Brandon', 31,  135, 'Salt Lake City', 'Yellow');	*/
                                                            
                                                            
                                                                /*--select *
                                                                --from person
                                                                --order by height desc
                                                                
                                                                --select *
                                                                --from person
                                                                --order by height asc
                                                                
                                                                --select * 
                                                                --from person
                                                                --order by age desc
                                                                
                                                                --select * 
                                                                --from person
                                                                --where age > 20
                                                                
                                                                --select * 
                                                                --from person
                                                                --where age = 18
                                                                
                                                                --select *
                                                                --from person 
                                                                --where age between 20 and 30
                                                                
                                                                --select *
                                                                --from person 
                                                                --where age != 27
                                                                
                                                                --select *
                                                                --from person
                                                                --where favorite_color != 'Red'
                                                                
                                                                --select * 
                                                                --from person 
                                                                --where favorite_color != 'Red' and favorite_color != 'Blue'
                                                                
                                                                --select * 
                                                                --from person
                                                                --where favorite_color = 'Orange' or favorite_color = 'Green'
                                                                
                                                                --select *
                                                                --from person
                                                                --where favorite_color in ('Orange', 'Green', 'Blue')
                                                                
                                                                --select *
                                                                --from person
                                                                --where favorite_color in ('Yellow', 'Purple')
                                                                
                                                                /*create table Orders 
                                                                (
                                                                person_id integer primary key autoincrement,
                                                                product_name text not null,
                                                                product_price integer not null,
                                                                quantity integer not null
                                                                )	*/
                                                                
                                                                /*	insert into orders (product_name, product_price, quantity)
                                                                values ('batteries', 22, 8);
                                                                
                                                                insert into orders (product_name, product_price, quantity)
                                                                values ('Disney Princess', 242, 3);
                                                                
                                                                insert into orders (product_name, product_price, quantity)
                                                                values ('Ballons', 5, 300);
                                                                
                                                                insert into orders (product_name, product_price, quantity)
                                                                values ('Water', 1, 1);
                                                                
                                                                insert into orders (product_name, product_price, quantity)
                                                                values ('Child Slaves', 120, 156135);	*/
                                                                
                                                                /*--select sum(quantity) 
                                                                --from orders
                                                                
                                                                --select sum(product_price)
                                                                --from orders
                                                                
                                                                --select sum(quantity * product_price)
                                                                --from orders 
                                                                --where person_id = 2
                                                                
                                                                /*	insert into artist (Name)
                                                                values ('Ryan');
                                                                insert into artist (Name)
                                                                values ('YaBoi');
                                                                insert into artist (Name)
                                                                values ('lil cool cool pump');	*/
                                                                
                                                                /*--select * 
                                                                --from artist
                                                                
                                                                --select *
                                                                --from artist
                                                                --order by Name desc 
                                                                --limit 10
                                                                
                                                            --    select * from artist order by Name limit 5
                                                            --	select * from artist where Name like 'Black%'
                                                                --select * from artist where name like '%Black%'
                                                                
                                                            --    select firstname, lastname from employee where city = 'Calgary';
                                                            --select firstname, lastname, birthdate from employee order by birthdate limit 1
                                                            --select firstname, lastname, birthdate from employee order by birthdate desc limit 1
                                                            --select * from employee where reportsto = 2
                                                            --select * from employee
                                                            --select count(*) from employee where city = 'Lethbridge'

                                                            --select count(*) from invoice where billingcountry = 'USA'
                                                            --select * from invoice order by total desc limit 1
                                                            --select * from invoice order by total limit 1
                                                            --select * from invoice where total > 5
                                                            --select * from invoice where total < 5
                                                            --select count(*) from invoice where billingstate in ('CA', 'TX', 'AZ') 
                                                            --select avg(total) from invoice 
                                                            --select sum(total) from invoice

### React-Redux
              // Set up you React app to use Redux:
                // Step 1: Create a 'ducks' folder in the 'src' folder. Then create a 'reducer.js' file in the 'ducks' folder.

                //  === REDUCER.JS ===
                const initialState = {
                // whatever you want to store in redux
                }

                // use default value/parameter for state
                // just return state for now
                export default function reducer(state = initialState, action) {
                return state
                }

                // ===================

                // Step 2: create the store
                // create a 'store.js' file in the src folder
                // what is below is all you will need for this file

                // === STORE.JS ===
                import { createStore } from 'redux';
                import reducer from './ducks/reducer';

                export default createStore(reducer);
                // =================

                // Step 3: user Provider to connect your React app to Redux

                // === INDEX.JS
                import React from 'react';
                import ReactDOM from 'react-dom';
                import './index.css';
                import App from './App';
                import * as serviceWorker from './serviceWorker';
                import { Provider } from 'react-redux';
                import store from './store';

                ReactDOM.render(
                <Provider store={store}>
                    <App />
                </Provider>
                , document.getElementById('root'));

                serviceWorker.unregister();

                // ==========

                // FROM HERE YOUR REACT APP CAN NOW ACCESS THE REDUX STORE

                // How do I get information from the redux store to my component?
                // step 1: connect the component
                // in the component file:
                import {connect} from 'react-redux';

                // the export the connected component
                // replace this line: 
                export default ComponentName;
                // with the following:
                export default connect()(ComponentName)

                // step 2: mapStateToProps
                // above the export, but outside of your class/function
                function mapStateToProps(state) {
                return state
                }
                // the key/value pairs from state will get added to the props object
                // then pass in mapStateToProps as the first argument to connect 
                export default connect(mapStateToProps)(ComponentName)

                // you can now access any property from the redux store on the props object

                // How do I update the redux store?

                // step 1:
                // create an action creator, a function that returns an action (object with type and payload properties)
                // export the action creator so that you can import it in the component file that you want to use it in 
                // update the reducer to use a switch statement. check for when the action.type matches what you are looking for.
                // return a new object. 
                // REMEMBER: treat your data as immutable
                // example of reducer.js file from the redux lecture


                // ACTION TYPES
                const ADD_TODO = 'ADD_TODO';

                // ACTION CREATORS
                export function addTodo(newTodo) {
                console.log('INSIDE ACTION CREATOR: ', newTodo)
                return {
                    type: ADD_TODO,
                    payload: newTodo
                }
                }

                // REDUCER
                export default function reducer(state = initialState, action) {
                console.log('reducer function running: ', action)
                switch (action.type) {
                    case ADD_TODO:
                    return { todos: [...state.todos, action.payload] }
                    default:
                    return state;
                }
                }


                // import your action creator to the component file you want to use it in and pass it in as the second argument for the connect method.
                // Note: the second argument in the connect method is an object with the action creators in it.
                // example:
                import React, { Component } from 'react';
                import './App.css';
                import { connect } from 'react-redux';
                import { addTodo } from './ducks/reducer';

                class App extends Component {
                constructor(props) {
                    super(props);
                    this.state = {
                    newTodo: ''
                    }
                }

                add() {
                    this.props.addTodo(this.state.newTodo);
                }

                render() {
                    console.log(this.props)
                    let todos = this.props.todos.map((todo, i) => {
                    return (
                        <div key={i}>
                        <p>{todo}</p>
                        </div>
                    )
                    })
                    return (
                    <div className="App">
                        <h1>My To-dos</h1>
                        <input onChange={(e) => this.setState({ newTodo: e.target.value })} type="text" />
                        <hr />
                        {todos}
                    </div>
                    );
                }
                }

                function mapStateToProps(reduxStore) {
                return reduxStore
                }

                export default connect(mapStateToProps, { addTodo })(App);