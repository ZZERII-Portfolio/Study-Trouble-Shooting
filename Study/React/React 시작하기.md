# ๐ฃReact ์์ํ๊ธฐ

๐ป๐จโ๐ป๐ฉโ๐ป๐ฉ๐ปโ๐ป๐จ๐ปโ๐ป๐พ๐คโฃโคโพโฝ๐จ๐ฌ๐ฏ๐ญโโโโ

## ๐ฅ์ฌ์ ์ค๋น

### โพ node JS

Node.js ๋ ์๋ฐ์คํฌ๋ฆฝํธ๊ฐ ๋ธ๋ผ์ฐ์  ๋ฐ(ex. ์๋ฒ)์์๋ ๋์ํ๊ฒ ํ๋ ํ๊ฒฝ์ ์๋ฏธํ๋ค.

```
> node -v
v14.16.0
```

โฝ ์ค์นํ๊ธฐ: https://nodejs.org/en/

**React ์ ํ๋ฆฌ์ผ์ด์์ ์น ๋ธ๋ผ์ฐ์ ์์ ์คํ๋๋ ์ฝ๋**์ด๋ฏ๋ก Node.js์ ์ง์ ์ ์ธ ์ฐ๊ด์ ์์ง๋ง, **ํ๋ก์ ํธ๋ฅผ ๊ฐ๋ฐํ๋ ๋ฐ ํ์ํ ์ฃผ์ ๋๊ตฌ๋ค(ex. babel, ์นํฉ)์ด Node.js ๊ธฐ๋ฐ์ด๊ธฐ ๋๋ฌธ์ ๋ฐ๋์ ์ค์น**ํด์ผ ํ๋ค.

### โพ npm

npm ์ Node Packaged Manager์ ์ค์๋ง๋ก Node๋ก ๋ง๋ค์ด์ง pakage ๋ค์ ๊ด๋ฆฌํด์ฃผ๋ ํด

๋ค์ํ ํจํค์ง๋ฅผ ์ค์นํ๊ณ  ๋ฒ์ ์ ๊ด๋ฆฌํ  ์ ์๋ค.

(python์ pip)

```
> npm -v
6.14.11
```

### โพ npx

npm์ 5.2.0 ๋ฒ์ ผ๋ถํฐ ์๋ก ์ถ๊ฐ๋ ๋๊ตฌ

```
> npx -v
6.14.11
```

์ค์นํ๊ธฐ:

```
> npm install npx -g
```



## ๐คReact App ์์ฑํ๊ธฐ



### โพ CRA(Create-React-App)

**: React ํ๋ก์ ํธ๋ฅผ ์์ํ๋๋ฐ ํ์ํ ๊ฐ๋ฐ ํ๊ฒฝ์ ์ธํ ํด์ฃผ๋ ๋๊ตฌ(toolchain)**

React๋ UI ๊ธฐ๋ฅ๋ง ์ ๊ณตํ๋ค. ๋ฐ๋ผ์ ๊ฐ๋ฐ์๊ฐ ์ง์  ๊ตฌ์ถํด์ผํ๋ ๊ฒ๋ค์ด ๋ง๋ค.

CRA๋ฅผ ์ด์ฉํ๋ฉด ํ๋์ ๋ช๋ น์ด๋ก React ๊ฐ๋ฐํ๊ฒฝ์ ๊ตฌ์ถํ  ์ ์๋ค.

CRA์๋ babel์ด๋ webpack๊ณผ ๊ฐ์ด React ์ ํ๋ฆฌ์ผ์ด์ ์คํ์ ํ์ํ ๋ค์ํ ํจํค์ง๊ฐ ํฌํจ๋์ด ์๋ค. 

>react ๋ฅผ ์ฌ์ฉํ๋ค๋ณด๋ฉด ES์ ์ต์ ๋ฒ์ ๊น์ง ์ฌ์ฉํด์ผ ํ๋ ๊ฒฝ์ฐ๊ฐ ์กด์ฌํ๋ค.
>
>ํ์ง๋ง ๋ช๋ช ๋ธ๋ผ์ฐ์ ์์๋, ํนํ IE ์์๋ ์ต์ ๋ฒ์ ์ ์ง์ํด์ฃผ์ง ์๋๋ค.
>
>๊ทธ๋ ๊ธฐ ๋๋ฌธ์ webpack ์ด๋ babel ๋ฑ ๊ณผ ๊ฐ์ ๋ช๋ช ๋ฐฉ๋ฒ์ด ํ์ํ๋ค.

 ํ์คํธ ์์คํ, ES6+ ๋ฌธ๋ฒ, CSS ํ์ฒ๋ฆฌ ๋ฑ ๊ฑฐ์ ํ์๋ผ๊ณ  ํ  ์ ์๋ ๊ฐ๋ฐ ํ๊ฒฝ๋ ๊ตฌ์ถํด ์ค๋ค.

์ด๋ฌํ ๊ฐ๋ฐ ํ๊ฒฝ์ ์ง์  ๊ตฌ์ถํ  ๊ฒฝ์ฐ ์๊ฐ์ด ์ค๋ ๊ฑธ๋ฆด ๋ฟ ์๋๋ผ ์ ์ง ๋ณด์๋ ํด์ผํ๋ค. CRA๋ฅผ ์ด์ฉํ๋ฉด ๊ฐ๋ฐ ํ๊ฒฝ ์ธํ์ ํด์ฃผ๊ธฐ ๋๋ฌธ์ ๊ธฐ์กด ๊ธฐ๋ฅ์ ๊ฐ์ ํ๊ฑฐ๋ ์๋ก์ด ๊ธฐ๋ฅ์ ์ถ๊ฐํ์ ๋ ํจํค์ง ๋ฒ์ ๋ง ์ฌ๋ฆฌ๋ฉด ๋๋ค.

> ### โพ ES (EMCAScript)
>
> EMCA์์ ๋ง๋  JavaScriptํ์ค์/ ์คํฌ๋ฆฝํธ ๊ท๊ฒฉ, ํ์ค
>
> #### ๋ฒ์  ๋ณ ํน์ง
>
> ##### โฝ ES3
>
> - ํํ ๋งํ๋ ์๋ฐ์คํฌ๋ฆฝํธ
>
> ##### โฝ ES5
>
> - ๋ฐฐ์ด์ forEach, map, filter, reduce, some๊ณผ ๊ฐ์ ๋ฉ์๋ ์ง์
> - Object์ ๋ํ getter / setter ์ง์
> - JSON ์ง์
>
> ##### โฝ ES6 (ES 2015)
>
> - let, const ํค์๋ ์ถ๊ฐ
>   - ๊ธฐ์กด์ ๋ณ์๋ ํจ์ scope๋ฅผ ๊ฐ์ง var ํค์๋๋ฅผ ์ด์ฉํ์์ต๋๋ค. ๋๋ฌธ์ block scope๋ฅผ ๊ฐ์ง let๊ณผ const ํค์๋๋ฅผ ์ถ๊ฐํ์ต๋๋ค.
> - arrow ๋ฌธ๋ฒ ์ง์
>   - arrow ๋ฌธ๋ฒ์ ๋๊ฐ์ง ์ฅ์ ์ด ์์ต๋๋ค. ์ฒซ์งธ, ํธํ๊ณ  ๊ฐ๊ฒฐํด์ง ์ฝ๋๋ฅผ ์์ฑํ  ์ ์์ต๋๋ค. ๋์งธ this๋ฅผ ๋ฐ์ธ๋ฉ ํ์ง ์์ต๋๋ค.
> - iterator / generator ์ถ๊ฐ
> - module import / export ์ถ๊ฐ
> - Promise ๋์
>
> ##### โฝ ES8 (ECMA 2017)
>
> - async - await ๋์



### โพ npm์ผ๋ก ์์ฑํ๊ธฐ

npx ๊ฐ ์กด์ฌํ์ง ์์์ ๊ฒฝ์ฐ์๋ npm์ ํตํด react app ์ ์์ฑ

```
npm install -g create-react-app
```

`-g`๋ฅผ ํตํด ์ ์ญ์ ์ผ๋ก `create-react-app`๊ฐ ์ค์น๋จ์ผ๋ก์ **์ฌ๋ฌ ๋ฌธ์ ์  ๋ฐ์**

- CRA์ ๋ฌด๊ฑฐ์ด ์์กด์ฑ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ค์ด ์ปดํจํฐ์ ๋จ๋๋ค
- CRA๋ฒ์  ์๋ฐ์ดํธ ์, ์ ์ญ์ ์ผ๋ก ์ค์น๋ CRA๋ฅผ ์ฌ์ค์น ํด์ผ ํ๋ค.



### โพ npx๋ก ์์ฑํ๊ธฐ

```
npx create-react-app {app์ด๋ฆ}
```

์ต์  CPAํจํค์ง๊ฐ ๋ค์ด๋ก๋ ๋๊ณ  ์ค์ ๋ค์ ์ธํํ ํ์ CRAํจํค์ง๋ ์ ๊ฑฐ๋๋ค.

๊ทธ๋ฌ๋ฏ๋ก ๋ฌด๊ฑฐ์ด ์์กด์ฑ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ค๋ ๋จ์ง ์๊ณ  ํจ๊ป ์ ๊ฑฐ๋๋ ์ด์ ์ด ์๋ค.



### โพ CRA๊ธฐ๋ณธ ํด๋ ๋ฐ ํ์ผ ๊ตฌ์ฑ

#### โฝ ์ด๊ธฐ ํด๋ ๋ฐ ํ์ผ ์ธํ ๊ตฌ์ฑ

##### :: node.modules / package.json / .gitignore

![image-20210325203809615](https://user-images.githubusercontent.com/61822411/112605132-4e7dcc00-8e5a-11eb-94f6-7079a00b6d43.png) 

**1) node.modules**

- CRA ๋ฅผ ๊ตฌ์ฑํ๋ ๋ชจ๋  **ํจํค์ง ์์ค ์ฝ๋๊ฐ ์กด์ฌ**ํ๋ ํด๋

![image-20210325204045968](https://user-images.githubusercontent.com/61822411/112605134-4f166280-8e5a-11eb-881a-a879e11e1273.png) 


**2) package.json**

- CRA ๊ธฐ๋ณธ ํจํค์ง ์ธ ์ถ๊ฐ๋ก ์ค์น๋ ๋ผ์ด๋ธ๋ฌ๋ฆฌ/ํจํค์ง ์ ๋ณด(์ข๋ฅ, ๋ฒ์ )๊ฐ ๊ธฐ๋ก๋๋ ํ์ผ

- ๋ชจ๋  ํ๋ก์ ํธ๋ง๋ค package.json ํ๋์ฉ ์กด์ฌ

- `"dependencies"`

  ![image-20210325204316937](https://user-images.githubusercontent.com/61822411/112605136-4f166280-8e5a-11eb-952b-50dfe42980f4.png)  

  - **๋ฆฌ์กํธ๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํ ๋ชจ๋  ํจํค์ง ๋ฆฌ์คํธ, ๋ฒ์  ํ์ธ ๊ฐ๋ฅ**
  - ์ค์  ์ฝ๋๋ `node.modules` ํด๋์ ์กด์ฌ

  

  - **์ node.modules ์ package.json ์์ ์ด์ค์ผ๋ก ํจํค์ง๋ฅผ ๊ด๋ฆฌํ ๊น?**

    - ์ค์  ๋ด๊ฐ ์์ฑํ ์ฝ๋, ๋ด๊ฐ ์ค์นํ ํจํค์ง๋ ๋ด ๋ก์ปฌ์๋ง ์กด์ฌํ๋ค.

    - github ์ ์ฌ๋ฆด ๋ ๋ด๊ฐ ์์ฑํ ์ฝ๋์ ํจ๊ป package.json(์ถ๊ฐ๋ก ์ค์นํ ํจํค์ง ์ ๋ณด)์ ๋๊ธด๋ค.

    - ๋ค๋ฅธ ์ฌ๋์ด ๊ทธ๊ฒ์ (pull) ๋ฐ์์ **npm install ๋ง ์๋ ฅํ๋ฉด package.json ์ ๊ธฐ๋ก๋์ด ์๋ ํจํค์ง์ ์ด๋ฆ๊ณผ ๋ฒ์  ์ ๋ณด๋ฅผ ํ์ธํ์ฌ ์๋์ผ๋ก ์ค์นํ๋ค.**

    - ์ด๋, github ์ ์ฌ๋ฆด ๋, node.modules ๋ ์ฌ๋ฆฌ๋ฉด ์๋๋ค. (๋ถํ์ํ ์ฉ๋ ์ฐจ์ง),

      ![image-20210325204658042](https://user-images.githubusercontent.com/61822411/112605137-4faef900-8e5a-11eb-8126-37d08ae27ba0.png) 

    - .gitignore ํ์ผ์ github ์ ์ฌ๋ฆฌ๊ณ  ์ถ์ง ์์ ํด๋์ ํ์ผ์ ์์ฑํ  ์ ์๋ค.

      

- **์ฐธ๊ณ ) ์๋ก์ด Library(package) ์ค์น ์**

  - ๋๊ตฐ๊ฐ ๋ง๋  ์์ค์ฝ๋๋ฅผ ๋ค์ด๋ฐ๋ ๊ฒ
  - npm์ผ๋ก ์ค์น (ex. npm install slider)
  - ์ค์น ์ node modules ์ ์๋์ผ๋ก ์ค์น๋จ.
  - ํ์ง๋ง **package.json - dependencies ์ ์ถ๊ฐ ์๋์ผ๋ก ๋๋ ๊ฑด ์๋**.
  - ๊ทธ๋์, `npm install slider --save`
  - --save ๊น์ง ์์ฑํด์ผ dependencies ์ ์ถ๊ฐ๋จ
  - (npm ๋ฒ์ ์ด ์๊ทธ๋ ์ด๋ ๋จ์ ๋ฐ๋ผ ์๋์ผ๋ก ์ถ๊ฐ๋๋ ๊ฒฝ์ฐ๊ฐ ๋ง์ง๋ง ์ฌ์ ํ ๋ถ์ํ ํจํค์ง๋ค์ด ์กด์ฌํ๊ธฐ ๋๋ฌธ์ ํจํค์ง ์ค์น ์ **--save ๊น์ง ์๋ ฅํ๋ ๊ฒ์ ๊ถ์ฅ**.)

- `"scripts"`

  ![image-20210325205222605](https://user-images.githubusercontent.com/61822411/112605129-4de53580-8e5a-11eb-85a7-5357885b5af9.png) 

  - `run` : ํ๋ก์ ํธ๋ฅผ development mode(๊ฐ๋ฐ ๋ชจ๋) ์คํ์ ์ํ ๋ช๋ น์ด. 

    `npm run start`.

  - `build` : ํ๋ก์ ํธ production mode(๋ฐฐํฌ ๋ชจ๋) ์คํ์ ์ํ ๋ช๋ น์ด. ์๋น์ค ์์ฉํ.

- ์ฐธ๊ณ ) [package.json vs. package-lock.json](https://www.youtube.com/watch?v=P2CtFD6xa54)

**3) package-lock.json**

- ํจํค์ง ๋ด๋ถ์ ํจํค์ง ๋ฒ์ ๊น์ง ๊ด๋ฆฌํด์ฃผ๋ ํ์ผ
- pull ์ดํ ์ถฉ๋์ ๋ง๋๋ค.

**4) .gitignore**

- `.gitignore` ํ์ผ์ **github ์ ์ฌ๋ฆฌ๊ณ  ์ถ์ง ์์ ํด๋์ ํ์ผ์ ์์ฑ**ํ  ์ ์๋ค.
- `push` ๋ฅผ ํด๋ `.gitignore` ํ์ผ์ ์์ฑ๋ ํด๋์ ํ์ผ์ ์ฌ๋ผ๊ฐ์ง ์๋๋ค.



##### :: public / src

**1) public ํด๋**

- index.html
- images - ์ด๋ฏธ์ง ํ์ผ ๊ด๋ฆฌ
- data - mock data ๊ด๋ฆฌ

**2) src ํด๋**

- components - ๊ณตํต ์ปดํฌ๋ํธ ๊ด๋ฆฌ
- pages - ํ์ด์ง ๋จ์์ ์ปดํฌ๋ํธ ํด๋๋ก ๊ตฌ์ฑ
- styles ํด๋
  - `reset.scss` - css ์ด๊ธฐํ
  - `commom.scss` - ๊ณตํต์ผ๋ก ์ฌ์ฉํ๋ css ์์ฑ ์ ์ (ex. font-family, theme color)
- ์ฐธ๊ณ ) components vs. pages
  - ์ฌ๋ฌ ํ์ด์ง์์ ๋์์ ์ฌ์ฉ๋๋ ์ปดํฌ๋ํธ์ ๊ฒฝ์ฐ components ํด๋์์ ๊ด๋ฆฌํจ.
    (ex. Header, Nav, Footer)
  - ํ์ด์ง ์ปดํฌ๋ํธ์ ๊ฒฝ์ฐ pages ํด๋์์ ๊ด๋ฆฌํจ.
  - ํด๋น ํ์ด์ง ๋ด์์๋ง ์ฌ์ฉํ๋ ์ปดํฌ๋ํธ์ ๊ฒฝ์ฐ ํด๋น ํ์ด์ง ์ปดํฌ๋ํธ ํด๋ ํ์์์ ๊ด๋ฆฌํจ.



##### :: index.html / index.js / App.js
