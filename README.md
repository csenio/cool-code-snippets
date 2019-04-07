# cool-code-snippets

## css

Easilly create and use media breakpoints in you arr like this:

const breakpoints = {
  mobileS: 320,
  mobileM: 375,
  mobileL: 425,
  tablet: 768,
  laptop: 1024,
  laptopL: 1440,
  desktop: 2560
};

export const breakpoint = Object.keys(sizes).reduce((acc, cur) => {
  acc[cur] = `(max-width: ${sizes[cur]}px)`;
  return acc;
}, {});
Make a separate breakpoints.js file import it in your styles.js and use it in your styled components like @media ${breakpoint.laptop}
