# React-player

`npm install react-player --save`

This contains the ` <ReactPlayer/> ` component which is makes configuring and controlling iframes easier in react.

the `playing` state can be passed as a prop to the player like such 
`<ReactPlayer url={url} playing={boolean}>`

Easy integration with react, because this means player props can be controled by react states or redux store. 

On ios, somehow the dispatch needs to happen in the same component for changing playing prop with redux store to work. Not sure why, might look into it later. 