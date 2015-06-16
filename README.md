# xamarin
Provides various libraries for making Xamarin.Forms development easier. Check out the [wiki](https://github.com/mikepham/xamarin/wiki) for more information.

Release: <a href="http://nativecode.no-ip.org:90/viewType.html?buildTypeId=xamarin_continuous&guest=1">
<img src="http://nativecode.no-ip.org:90/app/rest/builds/buildType:(id:xamarin_continuous)/statusIcon"/>
</a>

Continuous: <a href="http://nativecode.no-ip.org:90/viewType.html?buildTypeId=xamarin_release&guest=1">
<img src="http://nativecode.no-ip.org:90/app/rest/builds/buildType:(id:xamarin_release)/statusIcon"/>
</a>

## AppCompat
Simply install the NuGet package into your Android project.

`Install-Package NativeCode.Mobile.AppCompat`

Once installed, you should replace your *FormsApplicationActivity* derived activities with *AppCompatFormsApplicationActivity*.

For instance:

```csharp
public class MainActivity : AppCompatFormsApplicationActivity
{
  protected override void OnCreate(Bundle savedInstanceState)
  {
    base.OnCreate(savedInstanceState);

    Forms.Init(this, savedInstanceState);

    this.LoadApplication(new App());
  }
}
```

![screenshot-material-dark](screenshots/screenshot-material-dark.png)

You can then use the normal `Forms.Init` and `LoadApplication` methods to initialize your activities.

## AppCompat Renderers
Simply install the NuGet package into your Android project.

`Install-Package NativeCode.Mobile.AppCompat.Renderers`

Once installed, the renderers will be registered to replace the existing Xamarin.Forms renderers with ones that use the AppCompat controls, giving you Material Design elements.
