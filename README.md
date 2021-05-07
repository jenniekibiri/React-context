# React-context

```
import React from 'react'
const ThemeContext = React.createContext()

function App() {
  const [theme, setTheme] = useState('dark')

  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      <GrandChildComponent />
    </ThemeContext.Provider>
  )
}


function GrandChildComponent() {
  const { theme, setTheme } = useContext(ThemeContext)

  return (
    <>
      <div>The theme is {theme}</div>
      <button onClick={() => setTheme('light')}>
        Change To Light Theme
      </button>
    </>
  )
}
```


[React context code sandbox!](https://codesandbox.io/s/dark-moon-s7qi7?file=/src/App.js)
