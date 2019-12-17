[UP](./meta.md)

# viewport

<table>
    <tr>
        <td>Value</td>
		<td>Possible subvalues</td>
		<td>Description</td>
    </tr>
	<tr>
        <td>width</td>
		<td>A positive integer number, or the text device-width</td>
		<td>Defines the pixel width of the viewport that you want the web site to be rendered at</td>
    </tr>
	<tr>
        <td>height</td>
		<td>A positive integer, or the text  device-height</td>
		<td>Defines the height of the viewport. Not used by any browser</td>
    </tr>
	<tr>
        <td>initial-scale</td>
		<td>A positive number between 0.0 and 10.0</td>
		<td>Defines the ratio between the device width (device-width in portrait mode or device-height in landscape mode) and the viewport size</td>
    </tr>
	<tr>
        <td>maximum-scale</td>
		<td>A positive number between 0.0 and 10.0</td>
		<td>Defines the maximum amount to zoom in. It must be greater or equal to the minimum-scale or the behaviour is undefined. Browser settings can ignore this rule and iOS10+ ignores it by default</td>
    </tr>
	<tr>
        <td>minimum-scale</td>
		<td>A positive number between 0.0 and 10.0</td>
		<td>Defines the minimum zoom level. It must be smaller or equal to the maximum-scale or the behaviour is undefined. Browser settings can ignore this rule and iOS10+ ignores it by default</td>
    </tr>
	<tr>
        <td>user-scalable</td>
		<td>yes or no</td>
		<td>If set to no, the user is not able to zoom in the webpage. The default is yes. Browser settings can ignore this rule, and iOS10+ ignores it by default.</td>
    </tr>
</table>