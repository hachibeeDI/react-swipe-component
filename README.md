# react-swipe-component
Swipe bindings for react.

##Install
```
npm install react-swipe-component
```

##Usage
###Example
```
import React from 'react';
import ReactDOM from 'react-dom';
import Swipe from 'react-swipe-component';

const Home = React.createClass({
    render: function () {
        return (<Swipe 
                onSwipedLeft={this.onSwipeLeftListener} 
                onSwipedRight={this.onSwipeRightListener} 
                onSwipedDown={this.onSwipeDownListener} 
                onSwipedUp={this.onSwipeUpListener}>
            Demo
        </Swipe>);
    }
});

ReactDOM.render(<Home/>, document.getElementById('app') );
```

###Props
**```onSwipingUp```**, **```onSwipingRight```**, **```onSwipingDown```**, **```onSwipingLeft```**, are called with the event as well as the absolute delta of where the swipe started and where it's currently at. These constantly fire throughout touch events.

**```onSwipedUp```**, **```onSwipedRight```**, **```onSwipedDown```**, **```onSwipedLeft```** are called with the event as well as the x distance, + or -, from where the swipe started to where it ended. These only fire at the end of a touch event.

**```delta```** is the amount of px before we start firing events. Also affects how far onSwipedUp, onSwipedRight, onSwipedDown, and onSwipedLeft need to be before they fire events. The default value is 50.

**```preventDefaultEvent```** is whether to prevent the browser's touchmove event. Sometimes you would like the target to scroll natively. The default value is true.

**```nodeName```** is a string which determines the html element/node that this react component binds its touch events to then returns. The default value is 'div'.

#####PropTypes
```
  nodeName: React.PropTypes.string,
  onSwipingUp: React.PropTypes.func,
  onSwipingRight: React.PropTypes.func,
  onSwipingDown: React.PropTypes.func,
  onSwipingLeft: React.PropTypes.func,
  onSwipedUp: React.PropTypes.func,
  onSwipedRight: React.PropTypes.func,
  onSwipedDown: React.PropTypes.func,
  onSwipedLeft: React.PropTypes.func,
  delta: React.PropTypes.number,
  preventDefaultEvent: React.PropTypes.bool
```
##License
**MIT Licensed**
