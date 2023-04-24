https://swr.vercel.app/docs/pagination#when-to-use-useswr

Because of SWR's cache, we get the benefit to preload the next page. We render the next page inside a hidden div, so SWR will trigger the data fetching of the next page. When the user navigates to the next page, the data is already there:

```javascript
function App() {
  const [pageIndex, setPageIndex] = useState(0);

  return (
    <div>
      <Page index={pageIndex} />
      <div style={{ display: "none" }}>
        <Page index={pageIndex + 1} />
      </div>
      <button onClick={() => setPageIndex(pageIndex - 1)}>Previous</button>
      <button onClick={() => setPageIndex(pageIndex + 1)}>Next</button>
    </div>
  );
}
```

With just 1 line of code, we get a much better UX. The useSWR hook is so powerful, that most scenarios are covered by it.
