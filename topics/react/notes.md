# React notes

## How to get parameter values from query string in react-router

We can make use of the Web API _URLSearchParams_.

We can create a react hook that returns a new token.

```javascript
function useQuery() {
  return new URLSearchParams(useLocation().search);
}
```

An example hook from the [react-router docs](https://reactrouter.com/web/example/query-parameters).

One caveat is that URLSearchParams doesn't work in [older browsers](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams#Browser_compatibility).

_Extra reading_ [1](https://learnwithparam.com/blog/how-to-handle-query-params-in-react-router/), [2](https://stackoverflow.com/questions/35352638/react-how-to-get-parameter-value-from-query-string)

## Wait for API call to finish before rendering

`useEffect` will always execute after the first render, so a good way is to have a **Loader** while _asynchronous data_ is being fetched.

Another way is to pair a Loader with state that keeps track of data fetching.

```javascript
const [isBusy, setBusy] = useState(true);
```

_More reading_ [1](https://stackoverflow.com/questions/58956828/wait-for-api-call-data-before-render-react-hooks), [2](https://stackoverflow.com/questions/42132290/wait-for-react-promise-to-resolve-before-render)
