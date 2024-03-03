# React 17+/React-Query/Redux/React-Router Snippets README

Set of handy snippets for creating components using the latest syntax and best practices.

It also contains snippets for JavaScript, React-Query, Redux and React-Router.

Supports JavaScript and TypeScript files.

## JavaScript Snippets

| Snippet      | Renders                                    |
| ------------ | ------------------------------------------ |
| `imp`        | Named Import                               |
| `impD`       | Default Import                             |
| `impE`       | Import everything from module              |
| `impCss`     | Import css                                 |
| `impCssMod`  | Import css module styles                   |
| `impScssMod` | Import scss module styles                  |
| `cl`         | Print to the console                       |
| `clc`        | Print to the console from clipboard        |
| `cls`        | Log output to console from selected text   |
| `cd`         | Print to the console with dir              |
| `cdf`        | Print full data to the console with dir    |
| `cw`         | Print warning to the console               |
| `ce`         | Print error to the console                 |
| `deso`       | Destructure object                         |
| `desa`       | Destructure array                          |
| `fn`         | Function                                   |
| `arrow`      | Arrow function                             |
| `anon`       | Anonymous arrow function                   |
| `inline`     | Inline arrow function with implicit return |

## React Snippets

| Snippet | Renders                                           |
| ------- | ------------------------------------------------- |
| `rf`    | React functional component                        |
| `rfd`   | React Functional Component with default export    |
| `ra`    | React arrow functional component (named export)   |
| `rad`   | React arrow functional component (default export) |
| `lazy`  | Lazy component import                             |
| `eb`    | ErrorBoundary boilerplate                         |
| `us`    | useState Hook                                     |
| `usl`   | useState Hook with lazy init                      |
| `ured`  | useReducer Hook                                   |
| `ue`    | useEffect Hook                                    |
| `uec`   | useEffect Hook with clean function                |
| `ule`   | useLayoutEffect Hook                              |
| `ulec`  | useLayoutEffect Hook with clean function          |
| `ucx`   | useContext Hook                                   |
| `uc`    | useCallback Hook                                  |
| `um`    | useMemo Hook                                      |
| `uref`  | useRef Hook                                       |
| `uid`   | useId Hook                                        |
| `udv`   | useDeferredValue Hook                             |
| `ut`    | useTransition Hook                                |
| `uses`  | useSyncExternalStore Hook                         |

## React-Query Snippets

| Snippet | Renders               |
| ------- | --------------------- |
| `uq`    | useQuery Hook         |
| `umut`  | useMutation Hook      |
| `uqs`   | useQueries Hook       |
| `uiq`   | useInfiniteQuery Hook |
| `uqc`   | useQueryClient Hook   |

## React-Router Snippets

| Snippet | Renders                           |
| ------- | --------------------------------- |
| `unav`  | useNavigate Hook                  |
| `uh`    | useHistory Hook (react-router v5) |
| `up`    | useParams Hook                    |
| `uloc`  | useLocation Hook                  |

## Redux Snippets

| Snippet       | Renders                             |
| ------------- | ----------------------------------- |
| `usel`        | useSelector Hook                    |
| `uselshallow` | useSelector with shallow equal Hook |
| `ud`          | useDispatch Hook                    |
| `useStore`    | useStore Hook                       |

## Full Expansions

### JavaScript Snippets

#### `imp` - Named Import

```javascript
import { moduleName } from "module";
```

#### `impD` - Default Import

```javascript
import moduleName from "module";
```

#### `impE` - Import everything from module

```javascript
import * as moduleName from "module";
```

#### `impCss` - Import css

```javascript
import "./Component.css";
```

#### `impCssMod` - Import css module styles

```javascript
import styles from "./Component.module.css";
```

#### `impScssMod` - Import scss module styles

```javascript
import styles from "./Component.module.scss";
```

#### `cl` - Print to the console

```javascript
console.log(|);
```

#### `clc` - Print to the console from clipboard

```javascript
console.log(clipboard);
```

#### `cls` - Log output to console from selected text

```javascript
console.log("selected text");
```

#### `cd` - Print to the console with dir

```javascript
console.dir(|);
```

#### `cdf` - Print full data to the console with dir

```javascript
console.dir(|, { depth: null });
```

#### `cw` - Print warning to the console

```javascript
console.warn(|);
```

#### `ce` - Print error to the console

```javascript
console.error(|);
```

#### `deso` - Destructure object

```javascript
const { | } = object;
```

#### `desa` - Destructure array

```javascript
const [|] = array;
```

#### `arrow` - Arrow function

```javascript
const func = (param) => {
  return param;
};
```

#### `anon` - Anonymous arrow function

```javascript
(param) => {
  return param;
};
```

### React Snippets

<!-- prettier-ignore-start -->
#### `rf` - React functional component

```javascript
export function ComponentName() {
  return (
    <>
      |
    </>
  );
}
```

#### `ra` - React arrow functional component (named export)

```javascript
export const ComponentName = () => {
  return (
    <>
      |
    </>
  );
};
```


#### `rad` - React arrow functional component (default export)

```javascript
const ComponentName = () => {
  return (
    <>
      |
    </>
  );
};

export default ComponentName;
```

#### `lazy` - Lazy component import

```javascript
const ComponentName = lazy(() => import("./ComponentName"));
```

#### `eb` - ErrorBoundary boilerplate

```javascript
export class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError(error) {
    // Update state so the next render will show the fallback UI.
    return { hasError: true };
  }

  componentDidCatch(error, errorInfo) {
    // You can also log the error to an error reporting service
  }

  render() {
    if (this.state.hasError) {
      // You can render any custom fallback UI
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children;
  }
}
```

#### `us` - useState Hook

```javascript
const [state, setState] = useState(initialState);
```

#### `usl` - useState Hook with lazy init

```javascript
const [state, setState] = useState(() => fn);
```

#### `ured` - useReducer Hook

```javascript
const [state, dispatch] = useReducer(reducer, initialState);
```

#### `ue` - useEffect Hook

```javascript
useEffect(() => {
  |
}, []);
```

#### `uec` - useEffect Hook with clean function

```javascript
useEffect(() => {
  |
  return () => {
    |
  };
}, []);
```

#### `ule` - useLayoutEffect Hook

```javascript
useLayoutEffect(() => {
  |
}, []);
```

#### `ulec` - useLayoutEffect Hook with clean function

```javascript
useLayoutEffect(() => {
  |
  return () => {
    |
  };
}, []);
```

#### `ucx` - useContext Hook

```javascript
const context = useContext(Context);
```

#### `uc` - useCallback Hook

```javascript
const memoizedCallback = useCallback(callbackFn, []);
```

#### `um` - useMemo Hook

```javascript
const memoizedValue = useMemo(() => value, []);
```

#### `uref` - useRef Hook

```javascript
const ref = useRef(initialValue);
```

#### `uid` - useId Hook

```javascript
const id = useId();
```

#### `udv` - useDeferredValue Hook

```javascript
const deferredValue = useDeferredValue(value);
```

#### `ut` - useTransition Hook

```javascript
const [isPending, startTransition] = useTransition();
```

#### `uses` - useSyncExternalStore Hook

```javascript
const snapshot = useSyncExternalStore(subscribeFn, getSnapshotFn, getServerSnapshotFn);
```

### React-Query Snippets

#### `uq` - useQuery Hook

```javascript
const { | } = useQuery({ queryKey: [queryKey], queryFn: queryFn });
```

#### `umut` - useMutation Hook

```javascript
const { | } = useMutation({ mutationFn: mutationFn });
```

#### `uqs` - useQueries Hook

```javascript
const results = useQueries(
  list.map((item) => ({
    queryKey: ["", item],
    queryFn: queryFn,
  }))
);
```

#### `uiq` - useInfiniteQuery Hook

```javascript
const { | } = useInfiniteQuery({
  queryKey: ["key"],
  queryFn: ({ pageParam }) => queryFn,
  getNextPageParam: (lastPage) => getNextPageParam,
});
```

#### `uqc` - useQueryClient Hook

```javascript
const queryClient = useQueryClient();
```

### Redux Snippets

#### `ud` - useDispatch Hook

```javascript
const dispatch = useDispatch();
```

#### `usel` - useSelector Hook

```javascript
const state = useSelector((state) => state.state);
```

#### `uselshallow` - useSelector Hook with shallow equality check

```javascript
const state = useSelector((state) => state.state, shallowEqual);
```

### React-Router Snippets

#### `unav` - useNavigate Hook

```javascript
const navigate = useNavigate();
```

#### `up` - useParams Hook

```javascript
const { | } = useParams();
```

#### `uloc` - useLocation Hook

```javascript
const location = useLocation();
```

<!-- prettier-ignore-end -->
