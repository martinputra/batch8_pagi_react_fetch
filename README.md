## React Fetching data api

Okay teman teman kali ini kita akan belajar bagaimana caranya consume data dari api yang sudah pernah kita buat di sesi EXPRESS SQLITE dengan menggunakan REACT.

Pertama tentunya teman teman harus menjalankan server API di file express-sqlite uyang teman teman miliki.

```bash
cd express-sqlite
code .
npm run dev
```

Silakan buka **DBEAVER** dan teman teman bisa lihat di koneksi yang sebelumnya kita lakukan kita mempunyai sebuah table bernama **users** dan memiliki colums id, email, password dan created_at.

Pastikan server api sudah berjalan di port 8000, silakan test create dan read data users dengan file **test.rest**, apabila semuanya berjalan lancar, baru kita akan mulai code **REACT**

## Instalasi project React

Untuk mempermudah installasi project ini, silakan teman teman clone repository project ini saja, tanpa menginsatallnya lewat npm, npx atau yarn.

Buka terminal baru dan jalankan syntax ini di terminal.

```bash
git clone https://github.com/jemblonganvalley/batch8_pagi_react_fetch.git
cd bach8_pagi_react_fetch
yarn install
rm -rf .git
```

> syntax **yarn install** di jalankan Karena teman teman CLone dari sebuah repository git, teaman teman harus melakukan install environtment package yang tertera pada package.json.
> Tanpa melakukan ini, react teman tidak akan berjalan.

## Edit file app.js

Okay, yang pertama tama teman2 harus lakukan adalah mengedit file bernama App.js yang ada dalam folder src menjadi **App.jsx**

> JSX atau javascript extended adalah sebuah penambahan pada pemograman javascript yang memungkinkan kita bisa insert XML code langsung di dalam sintax javascript.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m2165c0w6zqcvgpsbljb.gif)

## React Hook State 
State adalah data private sebuah component. Data ini hanya tersedia untuk component tersebut dan tidak bisa di akses dari component lain. Component dapat merubah statenya sendiri.
[source](https://medium.com/coderupa/react-prop-state-apa-bedanya-7ee61df8257f)

Code state berada di dalam functional atau class component, karena kita tau **JVALLEY** menggunakan functional component, maka kita akan coba meletakan code hook useState pada component app kita.
<small>./src/App.jsx</small>
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0xe13o69hhcvx8s4uisj.gif)

Bisa teman teamn lihat di gif diatas, saya membuat sebuah Hook use state, dengan array literal
```javascript
const [data, setData] = React.useState([])
```
ada dua variable yang langsung saya buat didalam array, (array litteral), variable pertama bernama **data** merupakan variable penyimpan data state, dan variable kedua bernama **setData** merupakan sebuah function untuk merubah data pada variable pertama (data).
> Biasanya developer menulis state dengan function dispatch / function pengubah nilai state dengan urutan yang serupa, misal [siswa, setSiswa], [absen, setAbsen], [login, setLogin], dan seterusnya..

