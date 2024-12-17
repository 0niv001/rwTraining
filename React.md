---
sticker: lucide//atom
---
## Basics
- Front-end Library helps build UI from components.
- Components combine HTML and logic into a single *function. 
- All components go in JS files in src directory. 
- **JSX**: syntax extension allows to write Markup that looks like HTML. 
	- Explicitly close self closing elements. 
	- Components can only return a single element. 
- **App structure**: Single top level component called *App(). 
- Each component gets its own file, need to export (Default) it, before importing for render. 
- **Fragments** ``<> </> ``  empty tags with no HTML Elements
- Add {} to escape JSX and go to JS for evaluation. 
- Assign className to top level component to allow for styling and import css file
- **Vite** sets up React project automatically, run `npm create vite`

```JSX
export default function Dog({props="default"}){
	let numb = 2
	return <p className = "Dog"> {numb} {props.name}TEST!</p>
}
```

**Props**
- Arguments we can give components to make them configurable. 
- Can add as many as you want, just add space
- `<component props2 = {123} prop3 = {["blue", "red", "green"]}/>`

**Conditionals**
- Can use ternary operator inline and render HTML straight away. 
- `{x ==y ? <h1> content </> : <h1>Content</>}`
- `{x == y && <h1> content <h1/>}`

**Dynamic component styles**
- Provide CSS inline, using JS objects
- `const styles = {color: num1===num2 ? "red" : "green"}` and add to HTML using {}. 

**Rendering arr with Map**
- Do mapping inside html item. `arr.map(arr =)`