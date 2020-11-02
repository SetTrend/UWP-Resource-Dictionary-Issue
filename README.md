# UWP Resource Dictionary Issue

UWP documentation claims that styles can be applied to control
types as a whole, by providing a `TargetType` attribute:

- [UWP - ResourceDictionary and XAML resource references](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/resourcedictionary-and-xaml-resource-references)

However, that doesn't work.

So, I created this repository to provide a reproducable project,
demonstrating an issue with the UWP resource handling system.

In this repository I created a `ResourceDictionary` file (`Dictionary1.xaml`) to store a `Page`'s
background color. Next, I referenced that `ResourceDictionary` in my main page (`MainPage.xaml`).

While the Visual Studio 2019 (16.7.7) designer correctly renders the `Page`'s background color
in red, the running program itself doesn't.

#### Screenshot depicting the issue:

![UWP - unsuccessfully setting resources in XAML](https://i.stack.imgur.com/jQdYv.png)

## Verification

To verify this issue, I posted a corresponding question at
[StackOverflow](https://stackoverflow.com/questions/64617364/how-can-i-set-page-background-color-using-resouredictionary/64631649).

The result makes me believe that either the Microsoft documentation or the
implementation of UWP is faulty.

Before I report this issue to the Microsoft UWP product team, I'll jump off by reporting
this issue to the [Microsoft UWP documentation team](https://github.com/MicrosoftDocs/windows-uwp/issues/2790).