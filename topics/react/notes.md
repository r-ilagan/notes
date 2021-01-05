# React notes

## Wait for API call to finish before rendering

`useEffect` will always execute after the first render, so a good way is to have a **Loader** while _asynchronous data_ is being fetched.

Another way is to pair a Loader with state that keeps track of data fetching.

```javascript
const [isBusy, setBusy] = useState(true);
```

_More reading_ [1](https://stackoverflow.com/questions/58956828/wait-for-api-call-data-before-render-react-hooks), [2](https://stackoverflow.com/questions/42132290/wait-for-react-promise-to-resolve-before-render)
