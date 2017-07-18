# MEAN-STACK CRUD Use Angular2
 ## Project Overview
  ### Register
   <a href="http://www.mx7.com/view2/zZHJ5yyvDKqMtXHl" target="_blank">
    <img border="0" width="400" height="400" src="http://www.mx7.com/t/0d9/VNLyiV.png" />
   </a>

 ## How to run project
 1. สร้าง folder config ใน folder config สร้าง file ชื่อ config.js และ mongoose.js<br>
    <a href="http://www.mx7.com/view2/zZHryFJweBZoYCuj" target="_blank">
        <img border="0" width="300" height="300" src="http://www.mx7.com/i/22b/EecXAE.png" />
    </a><br>
Project นี้ผมใช้ data base ของ <a href="https://mlab.com/login/">mLap</a> โดยรูปแบบ uri จะเป็น mongodb://ชื่อผู้ใช้:รหัสผ่าน@ds161041.mlab.com:61041/ชื่อ collection
```sh
//config.js
module.exports = {
    uri: "<<you data base>>",// ใช้ได้ทั้ง database ในเครื่อง หรือ จากบริการของเว็ปไซต์
    secret: "<<you secret password>>"//ใช้ตัวเลขตัวอักษรได้ตามใจชอบ
}
```
```sh
// mongoose.js
var config = require('./config')
var mongoose = require('mongoose')
module.exports = function(){
    var db = mongoose.connect(config.uri);
    return db;
}
```
        
 2. Download dependencies ใช้คำสั่ง <code>npm install </code> จากนั้น สั่ง Start project ใช้คำสั่ง <code>npm start</code> 

 ## FontEnd(Angular2)
| Topic                         | Description                                 | Link Detailed                            |
|:---------------------------------:|:-------------------------------------------:|:-----------------------------------|
| ARCHITECTURE OVERVIEW |อธิบายเบื้องต้นเกี่ยวกับ Components, Templates, Metadata, Data-binding, Directives, Services, Dependency-injection    |[Architecture](angular-src/README/archetecture/README.md)|
| Driven Forms | Login ใช้ Diven Forms ในการจัดการ |[Login(FontEnd)](angular-src/src/app/components/login/README.md)|
| Reactive Forms| Register ใช้ Reactive Forms  ในการจัดการ |[Register(FontEnd)](angular-src/src/app/components/register/README.md)|
| RESTful API   | ใช้ RESTfull API ในการทำงาน ระบุตัวตนผ่าน Token(JWT) และจัดเก็บ Password โดยการเข้ารหัสด้วย Becrypt |[RESTful API](angular-src/README/RESTful/README.md)|
| Http Service  | Http service and custom ให้ทุกๆ request ที่ส่งออกไปโยน Token ใส่ Http header ไปด้วย |[Http service](angular-src/README/HTTP/README.md)                         |
| Router |                                      |                                    |
| Guard             |                                             |                                    |
| Proxy              |                                             |                                    |


 ## BackEnd(MVC)
 - Express (Routing)
 - Nodejs (Controller)
 - MongoDB,Mongoose (Model)

| Topic                         | Description                                 | Link Detailed                            |
|:---------------------------------:|:-------------------------------------------:|:-----------------------------------|
| What is MVC| MVC ย่อมาจาก Model View Controller  |                                    |
| MVC Folder By Feature | รูปแบบการแบ่ง Folder ตาม Feature ที่ทำงานเพื่อให้จัดการข้อมูลอย่างเป็นระบบ|                                    |
| NodeJs login/Register |ประกอบไปด้วยการจัดการ routing controller และ models |[Login/Register(BackEnd)](app/users/README.md)|
| Express Routing | เทคนิคการเขียน Routing ให้สามารถใช้ประโยชน์ จาก concept foder by feature |                                    |
| Mongoose Paginate            |                                             |                                    |

## Create
## Read/Render
## Update
## Delete