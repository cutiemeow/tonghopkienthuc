# React-router-dom
**react-router đã tách ra thành 3 package nhỏ**
- react-router-dom: dành cho web
- react-router-native: cho mobile
- react-router-core: cho các ứng dụng lõi

**cài đặt dependency**
```$ npm install --save react-router-dom ```

**import component "BrowerRouter", "Link", "Route"**

`import { BrowserRouter, Route, Link } from 'react-router-dom'`

## Link
**Link được sử dụng để điều hướng. Nó tương đương với thẻ `<a>`, Tham số truyền vào Link là to, nhận đường dẫn url**
    
    <ul>
    <li><Link to="/">Home</Link></li>
    <li><Link to="/about">About</Link></li>
    <li><Link to="/topics">Topics</Link></li>
    </ul>
    
## Route
**Là một component con chịu trách nhiệm render UI, dựa trên location người dùng truyền vào**
**`<Router>` định nghĩa View theo 2 cách:**
  - Tạo Component được chỉ định trong `<Route>`
  - Sử dụng hàm `render()`
  
`<Route>` sẽ trả về null trong trường hợp url nhập vào không trùng với path định nghĩa
`<Route>` nhận vào hai tham số : 1 là path 2 là component sẽ render

    <BrowserRouter>
      <div>
        <Route exact path="/" render={ ( ) => (<h2> HomePage </h2>) } />
        <Route path="/about" component={About}/>
        <Route path="/topics" component={Topics}/>
      </div>
    </BrowserRouter>


**Ở ví dụ trên nếu không sử dụng exact, đường dẫn "/" sẽ macth với cả "/about", "/topic"**

**Phải gói tất cả route vào một thẻ `<div>` nếu không sẽ báo lỗi**

**Ví dụ**

    <BrowserRouter>
      <div>
        <ul>
         <li><Link to="/">Home</Link></li>
         <li><Link to="/about">About</Link></li>
         <li><Link to="/topics">Topics</Link></li>
        </ul>
        <Route exact path="/" render={ ( ) => (<h2> HomePage </h2>) } />
        <Route path="/about" component={About}/>
        <Route path="/topics" component={Topics}/>
      </div>
    </BrowserRouter>
