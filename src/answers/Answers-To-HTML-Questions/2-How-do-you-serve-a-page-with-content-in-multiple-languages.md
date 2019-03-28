# How do you serve a page with content in multiple languages ?
Use utf-8 encoding to serve a page with multiple languages.

 - Specify response header `content-type: text/html; charset=UTF-8`
 - Post data with `application/x-www-form-urlencoded;charset=utf-8`
 - Source files should be set with utf-8 without BOM
 - Database should be set with utf-8. For example MySQL: `SET NAMES utf8mb4 COLLATE utf8mb4_unicode_ci`
 - Use `lang` HTML attribute if neccessary
 
 
### References
 - https://www.quora.com/How-can-I-serve-a-page-with-content-in-multiple-languages
 - https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang
 - https://docs.lvrui.io/2016/08/21/%E4%BF%AE%E6%94%B9MySQL%E7%9A%84%E5%AD%97%E7%AC%A6%E9%9B%86%E4%B8%BAutf8mb4/
