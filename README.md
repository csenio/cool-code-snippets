# cool-code-snippets

## css

### Easy media breakpoints for css in js (credit to [zlobic](https://github.com/zlobic))
```
const breakpoints = {
  mobile: 320,
  tablet: 768,
  laptop: 1024,
  laptopL: 1440,
  desktop: 2560
}

for(i in breakpoints){
  breakpoints[i]=`all and (max-width: ${breakpoints[i]}px)`
}

export default breakpoints
```
Make a separate breakpoints.js file import it in your styles.js and use it in with styled components
```
@media ${breakpoints.laptop}
```
### Scroll to top when going to a new page with react router
     ```
     <Route path="/" component={scrollToTop} />
     
     const scrollToTop = () => {
     window.scrollTo(0, 0)
     return null;
     };
     ```
### reduce until index
```
const reduceUntil = (arr,index)=> arr.slice(0,3).reduce((acc,val)=>acc + val)
```

### create an array from x ... n
```
Array.from(Array(n).keys()).map(n => n + x);
```

### get all images (or other files) from a folder (webpack)
```
function importAll(r) {
  return r.keys().map(r);
}

const images = importAll(
  require.context("./images", false, /\.(png|jpe?g|svg)$/)
);
```
