# Contacts
* Full name: Igor Zavirukhin
* E-mail: mrertert@gmail.com
* Github: [@Ursa1337](https://github.com/Ursa1337)
* Phone: [+375445811602](tel:375445811602)

# About Me
I can communicate in a team, solve problems quickly, learn something new. My goal is to learn javascript for backend and frontend development. My priority is to learn English

# Skills
* HTML, CSS
* Javascript
    * React
    * Redux
    * NestJS (microservices)
    * NextJS (SPA, SSR)
    * Sequelize
    * Aws-sdk (s3)
    * Mongoose
* C (basic)
* Python (basic)
* RabbitMQ
* PostgreSQL
* MongoDB
* S3
* Docker

# Code example
```
class FileJPEGSizeValidator extends FileValidator<ImageSizeType> {
  buildErrorMessage(): string {
    return `Validation failed (expected width ${this.validationOptions.height}px and height ${this.validationOptions.width}px)`
  }

  isValid(file: any): boolean {
    //SOF part include width and height image. SOF start from FF C0.
    //height contains SOF + 4 offset, width contains SOF + 6 offset.
    const index = file.buffer.indexOf('ffc0', 0, 'hex')
    if (index) {
      const bufferHeight = file.buffer.slice(index + 5, index + 7)
      const bufferWidth = file.buffer.slice(index + 7, index + 9)
      if (
        Buffer.byteLength(bufferHeight) === 2 &&
        Buffer.byteLength(bufferWidth) === 2 &&
        bufferHeight.readUInt16BE(0) === this.validationOptions.height &&
        bufferWidth.readUInt16BE(0) === this.validationOptions.width
      ) {
        return true
      }
    }
  }
}
```

# Courses
* [Javascript (in progress)](https://rs.school/js/)
* [HTML/CSS/JS](https://www.udemy.com/course/webdeveloper/)

# Languages
* Russian - Native
* English - A2