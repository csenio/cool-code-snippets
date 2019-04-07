# cool-code-snippets

## css

Easilly create and use media breakpoints in you arr like this:
```
const breakpoints = {
  mobile: 320,
  tablet: 768,
  laptop: 1024,
  laptopL: 1440,
  desktop: 2560
}

for(i in breakpoints){
  breakpoints[i]=`all and (max-width: ${i}px)`
}

export default breakpoints
```
Make a separate breakpoints.js file import it in your styles.js and use it in with styled components
```
@media ${breakpoints.laptop}
