# What are the various clearing techniques and which is appropriate for what context ?
 - Add `overflow: auto` to container element
 - Add clearfix class to container element
 - Use `flexbox` instead when available
 - Use `grid` instead when available
 
 ```css
.clearfix:after {
	visibility: hidden;
	display: block;
	font-size: 0;
	content: " ";
	clear: both;
	height: 0;
}
* html .clearfix { zoom: 1; } /* IE6 */
*:first-child+html .clearfix { zoom: 1; } /* IE7 */
 ```
 
 ### References
  - https://perishablepress.com/better-clearfix/
