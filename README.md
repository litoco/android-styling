# android-styling

**Style** are the set of attributes that are applied to a single view\
**Theme** is a collection of attributes that are applied to the entire application and not one view.
For more on styles vs theme go [here](https://medium.com/androiddevelopers/android-styling-themes-vs-styles-ebe05f917578).

**Style:**\
A style is declared in the `res/values` folder(typically inside the `styles.xml` or `themes.xml` file). Following is the way of adding styles in android:
```
<style name="..." parent="...">
  <item name="....">value</item>
  ...
  ...
  ...
</style>
```
Here, `name` attribute of `style` tag can be anything that you want to give. `parent` attribute is the library or the attribute that you want to inherit from.\
Eg:
```
  parent="@android:style/TextAppearance"
  parent="Widget.MaterialComponents.Button"<!-- If you want to style a material component button -->
```
`parent` attribute should be provided for better functioning of the application.

The `<item>` tag inside `<style>` function as a key value pair. The key is the `name` attribute and its value is put inside the `<item>` tag.

Eg:
```
<item name="android:textColor">#00FF00</item>
<item name="android:background">#000000</item>
```
`name` in each `item` specifies an attribute you would otherwise use as an XML attribute in your layout

**Theme:**\
It is also declared as `<style>` tag but is way different than it.\
If you want to apply some style to all elements of the application, you must include it in the theme.\
Eg: If you want to specify that a style named *myStyle* should be applied all across the application then, see the following code:
```
<style name="MyAppTheme" parent="Theme.MaterialComponents.DayNight.NoActionBar">
  ...
  <item name="myCustomStyle">@style/myStyle</item>
  ...
</style>
```
**Congratulations!!!** You have successfully added a style to your application.
For more information visit [android developer site](https://developer.android.com/guide/topics/ui/look-and-feel/themes#top_of_page)
