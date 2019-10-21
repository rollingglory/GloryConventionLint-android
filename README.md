
<img align="left" width="60" height="60" src="https://avatars1.githubusercontent.com/u/30823810?s=100&v=4"> </img>

**RollingGlory** is Company or Creative Digital Media studio based in Bandung, Indonesia.


&nbsp;
&nbsp;
## GloryConventionLint-android
GloryConventionLint is judgment code for Convention lint in IDE Android Studio support java and kotlin.

#### Link for Configuration Gradle
* [Configuration gradle for Module](#configuration-gradle-for-module)
* [Configuration gradle for Project](#configuration-gradle-for-project)

#### Convention 
* [CamelCase Convention](#camelcase-convention)
* [CapitalizationCase Convention](#capitalizationcase-convention)
* [ClassCase Convention](#classcase-convention)
* [ConstantCase Convention](#constantcase-convention)
* [MethodCase Convention](#methodcase-convention)
* [XmlCase Convention](#xmlcase-convention)
* [XmlIDCase Convention](#xmlidcase-convention)

#### Example
* [Example Report Issue CamelCase](#example-report-issue-camelcase)
* [Example Report Issue MethodCase](#example-report-issue-methodcase)
* [Example Report Issue ClassCase](#example-report-issue-classcase)

#### FAQ 
* [Frequently Asked Questions](#frequently-asked-questions)

#### Next to do  
* [XmlValueCase Convention](#xmlvaluecase-convention)
* [GradleModuleCase Convention](#gradlemodulecase-convention)
* [GradleProjectCase Convention](#gradleprojectcase-convention)

&nbsp;
---
&nbsp;
#### Configuration Gradle for Module
Don't forget, configuration gradle your must use ***lintChecks***, don't use *implementation, kapt or api*.
~~~gradle
dependencies {
   lintChecks 'com.rollingglory:gloryconventionlint-android:0.0.3'
}
~~~


#### Configuration Gradle for Project
~~~gradle

allprojects {
    repositories {
      maven {
            url  "https://dl.bintray.com/rollingglory/GloryConventionLint-android"
        }
    }
}

~~~


## Convention
#### CamelCase Convention
Example phrase : *areInject, whatFlavor, loadMore*

<table>
    <tbody>
        <tr>
           <td rowspan=2>&nbsp;</td>
           <td colspan=3 align=center> <strong>LOCAL</strong> </td>
           <td colspan=3 align=center> <strong>GLOBAL</strong> </td>
        </tr>
         <tr>
           <td>variable</td>
           <td>method</td>
            <td>class</td>
           <td>variable</td>
           <td>method</td>
           <td>class</td>
        </tr>
        <tr>
           <td>not final</td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td>:heavy_check_mark:</td>
            <td></td>
        </tr>
        <tr>
           <td>not static</td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td>:heavy_check_mark:</td>
            <td></td>
        </tr>
         <tr>
           <td>not final static</td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td>:heavy_check_mark:</td>
            <td></td>
        </tr>
        <tr>
           <td>final</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
           <td>static</td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td>:heavy_check_mark:</td>
            <td></td>
        </tr>
        <tr>
            <td>final static</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

&nbsp;
&nbsp;

#### CapitalizationCase Convention
Example phrase : *LoginActivity, UserFragment, UserSession*

<table>
    <tbody>
        <tr>
           <td rowspan=2>&nbsp;</td>
           <td colspan=3 align=center> <strong>LOCAL</strong> </td>
           <td colspan=3 align=center> <strong>GLOBAL</strong> </td>
        </tr>
         <tr>
           <td>variable</td>
           <td>method</td>
            <td>class</td>
           <td>variable</td>
           <td>method</td>
           <td>class</td>
        </tr>
        <tr>
           <td>not final</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
        <tr>
           <td>not static</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
         <tr>
           <td>not final static</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
        <tr>
           <td>final</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
        <tr>
           <td>static</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
        <tr>
            <td>final static</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
    </tbody>
</table>

&nbsp;
&nbsp;

#### ClassCase Convention
If you create class extends of table below, use this convention.

<table>
    <tbody>
         <tr>
            <td rowspan=2><b>Extends Of</b></td>
            <td rowspan=2><b>Package's</b></td>
            <td colspan=2 align=center><b>Naming Convention</b></td>
            <td rowspan=2><b>Example Phrase</b></td>
        </tr>
        <tr>
            <td><b>PreFix</b></td>
            <td><b>PostFix</b></td>
        </tr>
        <tr>
            <td>AppCompatActivity</td>
            <td>androidx.appcompat.app<br/>android.support.v7.app</td>
            <td></td>
            <td>Activity</td>
            <td><i>Yourname<b>Activity</b><i></td>
        </tr>
         <tr>
            <td>Activity</td>
            <td>android.app</td>
            <td></td>
            <td>Activity</td>
            <td><i>Yourname<b>Activity</b><i></td>
        </tr>
       <tr>
            <td>ActivityGlory</td>
            <td>com.rollingglory.glorysdk.layer</td>
            <td></td>
            <td>Activity</td>
            <td><i>Yourname<b>Activity<b><i></td>
        </tr>
       <tr>
            <td>Fragment</td>
            <td>android.support.v4.app.Fragment<br/>androidx.fragment.app.Fragment</td>
            <td></td>
            <td>Fragment</td>
            <td><i>Yourname<b>Fragment<b></i></td>
        </tr>   
        <tr>
            <td>FragmentGlory</td>
            <td>com.rollingglory.glorysdk.layer</td>
            <td></td>
            <td>Fragment</td>
            <td><i>Yourname<b>Fragment<b></i></td>
        </tr>        
        <tr>
            <td>Service</td>
            <td>android.app</td>
            <td></td>
            <td>Service</td>
            <td><i>Yourname<b>Service<b></i></td>
        </tr>   
        <tr>
            <td>ServiceGlory</td>
            <td>com.rollingglory.glorysdk.layer</td>
            <td></td>
            <td>Service</td>
            <td><i>Yourname<b>Service<b></i></td>
        </tr>  
   </tbody>
</table>
               
&nbsp;
&nbsp;


#### ConstantCase Convention
Example phrase : *SCOPE_USER, SIZE_BLOCK, POSTION_DEFAULT*
<table>
    <tbody>
        <tr>
           <td rowspan=2>&nbsp;</td>
           <td colspan=3 align=center> <strong>LOCAL</strong> </td>
           <td colspan=4 align=center> <strong>GLOBAL</strong> </td>
        </tr>
         <tr>
           <td>variable</td>
           <td>method</td>
            <td>class</td>
           <td>variable</td>
           <td>method</td>
           <td>class</td>
            <td>enum</td>
        </tr>
        <tr>
           <td>not final</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
           <td>:heavy_check_mark:</td>
        </tr>
        <tr>
           <td>not static</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
         <tr>
           <td>not final static</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
        </tr>
        <tr>
           <td>final</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
              <td></td>
        </tr>
        <tr>
           <td>static</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
              <td></td>
        </tr>
        <tr>
            <td>final static</td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
            <td>:heavy_check_mark:</td>
            <td></td>
            <td></td>
           <td></td>
        </tr>
    </tbody>
</table>

&nbsp;
&nbsp;
#### MethodCase Convention
If class extends AppCompatActivity, you should override method ***onCreate(Bundle savedInstanceState)*** first sequence.
~~~java
class HomeActivity extends AppCompatActivity{
   //onCreate method should first squence in class
   @Override
   protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
   }
   
   @Override
   protected void onPause() {
     super.onPause();
   }

   @Override
   protected void onResume() {
     super.onResume();
   }
~~~
&nbsp;
&nbsp;
#### XmlCase Convention
<table>
    <tbody>
         <tr>
            <td rowspan=2><b>Resource</b></td>
            <td colspan=2 align=center><b>Naming Convention</b></td>
            <td rowspan=2><b>Example Phrase</b></td>
        </tr>
        <tr>
            <td><b>PreFix's</b></td>
            <td><b>PostFix's</b></td>
        </tr>
        <tr>
            <td>Layout</td>
            <td>activity_<br/>fragment_<br/>layout_<br/>item_<br/>dialog_</br>partial_</td>
            <td></td>
           <td><i><b>fragment_</b>login<i></td>
        </tr>
        <tr>
            <td>Drawable</td>
            <td>ic_<br/>bg_<br/></td>
            <td></td>
            <td><i><b>ic_</b>notification<i></td>
        </tr>
        <tr>
            <td>Menu</td>
            <td>menu_<br/></td>
            <td></td>
            <td><i><b>menu_</b>dashboard<i></td>
        </tr>
        <tr>
            <td>Font</td>
            <td><br/></td>
           <td>-regular<br/>-bold</br>-italic</td>
            <td><i>robot<b>-regular</b><i></td>
        </tr>
   </tbody>
</table>
   
&nbsp;
&nbsp;

#### XMLIDCase Convention

<table>
    <tbody>
         <tr>
            <td rowspan=2><b>Extends Of</b></td>
            <td rowspan=2><b>Package's</b></td>
            <td colspan=2 align=center><b>ID Convention</b></td>
            <td rowspan=2><b>Example ID</b></td>
        </tr>
        <tr>
            <td><b>PreFix</b></td>
            <td><b>PostFix</b></td>
        </tr>
        <tr>
            <td>TextView</td>
            <td>android.widget.TextView</td>
            <td>@+id/tv_</td>
            <td></td>
            <td><i>@+id/tv_<b>yourid</b><i></td>
        </tr>
       <tr>
            <td>Button</td>
            <td>android.widget.Button</td>
            <td>@+id/btn_</td>
            <td></td>
            <td><i>@+id/btn_<b>yourid</b><i></td>
        </tr>
        <tr>
            <td>ImageView</td>
            <td>android.widget.ImageView</td>
            <td>@+id/iv_</td>
            <td></td>
            <td><i>@+id/iv_<b>yourid</b><i></td>
        </tr>
        <tr>
            <td>LinearLayout<br/>RelativeLayout<br/>CoordinatorLayout</td>
            <td>android.widget.LinearLayout<br/>android.widget.RelativeLayout<br/>android.support.design.widget.CoordinatorLayout<br/>androidx.coordinatorlayout.widget.CoordinatorLayout</td>
            <td>@+id/content_</td>
            <td></td>
            <td><i>@+id/content_<b>yourid</b><i></td>
        </tr>
   </tbody>
</table>
               
&nbsp;
&nbsp;              

## Example
#### Example Report Issue CamelCase
<img src="https://github.com/rollingglory/GloryConventionLint-android/blob/master/resource/camelcase.png"> </img>

&nbsp;
&nbsp;

#### Example Report Issue MethodCase
<img src="https://github.com/rollingglory/GloryConventionLint-android/blob/master/resource/methodcase.png"> </img>

&nbsp;
&nbsp;

#### Example Report Issue ClassCase
<img src="https://github.com/rollingglory/GloryConventionLint-android/blob/master/resource/classcase.png"> </img>

&nbsp;
&nbsp;



## Frequently Asked Questions
#### Can this work for java and kotlin languages?
*GloryConventionLint will automatically create rules for both languages.*

#### Can this be used for projects in my company?
Please this can be used for your company's project, with MIT License.

#### Does this work for an intellij java IDE?
*This might work for the Java Intelij IDE, but it's more recommended to use Intelij Android Studio*

#### Does this work for all versions of IDE Android Studio?
*This works for android studio 3.x.x, if you still use android studio 2.x.x please open ***Next to do***

&nbsp;
&nbsp;
## Next to do
#### Link for android version 2.x.x
#### XMLValueCase Convention
#### GradleModuleCase Convention
#### GradleProjectCase Convention

&nbsp;
&nbsp;

### Other Information
You can follow us at <https://rollingglory.com/>

