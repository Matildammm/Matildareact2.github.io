# Matildareact
//profile

import { GrMail  } from "react-icons/gr";
import '../App.css';

const profile = () => {
    return(
        <div className="box">
        <h2>Contact Details</h2>
        <ul>
            <li>0711193176 </li>
            <li>maphutimatilda7@gmail.com</li>
            <li>0711193176 </li>
            <li>Matilda </li>
        </ul>
</div>
    )
}
export default profile

//about 
import React from 'react';
import '../App.css';

const about = () => {
    return(
        <div className="box">
        <h2>M resume v</h2>
        </div>
    )
}
export default about

//menu 
import React from 'react';
import { BrowserRouter as Router, Link, NavLink, Route, Switch } from 'react-router-dom';
import Profile from './profile';
import About from './about';
import Users from './users';
import Landing from './landing';
import '../App.css';

const menu = () => {
    return (
        <>
        <Router>
            <div>
                <nav className = "navigation">
                    <ul>
                        <li>
                            <Link to='/'>Home</Link>
                        </li>
                        <li>
                            <Link to='/about'>About</Link>
                        </li>
                        <li>
                            <Link to='/profile'>Profile</Link>
                        </li>
                        <li>
                            <Link to='/users'>Users</Link>
                        </li>
                    </ul>
                </nav>

<Switch>
    <Route path='/profile'>
<Profile/>
    </Route>
    <Route path='/about'>
<About/>
    </Route>
    <Route path='/users'>
       <Users/> 
        </Route>  
        <Route path='/'>
            <Landing/>
            </Route>  
</Switch>
            </div>
        </Router>
        </>
    )
}
export default menu; 

//home
import React, {Component} from 'react';
import Menu from './menu'

export default class home extends Component {
    render(){
        return(
            <>
            <Menu/>
            </>
        )
    }
} 

//landing
import React from 'react';


const landing = () => {
        return(
            <div className="box">
                <h1>Welcome to my page</h1>
            </div>
        )
}
export default landing 

//index


import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';
import Home from './component/home';

ReactDOM.render( <
    React.StrictMode >
    <
    Home / >
    <
    /React.StrictMode>,
    document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals(); 

