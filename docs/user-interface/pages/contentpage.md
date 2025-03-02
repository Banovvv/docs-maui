---
title: "ContentPage"
description: "The .NET MAUI ContentPage displays a single view, which is often a layout, and is the most common page type."
ms.date: 03/14/2022
---

# ContentPage

:::image type="content" source="media/contentpage/pages.png" alt-text=".NET MAUI ContentPage." border="false":::

The .NET Multi-platform App UI (.NET MAUI) `ContentPage` displays a single view, which is often a layout such as as `Grid` or `StackLayout`, and is the most common page type.

[!INCLUDE [docs under construction](~/includes/preview-note.md)]

`ContentPage` defines a `Content` property, of type `View`, which defines the view that represents the page's content. This property is backed by a `BindableProperty` object, which means that it can be the target of data bindings, and styled. In addition, `ContentPage` inherits `Title`, `IconImageSource`, `BackgroundImageSource`, `IsBusy`, and `Padding` bindable properties from the `Page` class.

> [!NOTE]
> The `Content` property is the content property of the `ContentPage` class, and therefore does not need to be explicitly set from XAML.

.NET MAUI apps typically contain multiple pages that derive from `ContentPage`, and navigation between these pages can be performed. For more information about page navigation, see [NavigationPage](navigationpage.md).

A `ContentPage` can be templated with a control template. For more information, see [Control templates](~/fundamentals/controltemplate.md).

## Create a ContentPage

To add a `ContentPage` to a .NET MAUI app:

1. In **Solution Explorer** right-click on your project or folder in your project, and select **New Item...**.
1. In the **Add New Item** dialog, expand **Installed > C# Items**, select **.NET MAUI**, and select the **.NET MAUI ContentPage (XAML)** item template, enter a suitable page name, and click the **Add** button:

    :::image type="content" source="media/contentpage/item-template.png" alt-text=".NET MAUI ContentPage item template.":::

Visual Studio then creates a new `ContentPage`-derived page, which will be similar to the following example:

```xaml
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="MyMauiApp.MyPage"
             Title="MyPage"
             BackgroundColor="White">
    <StackLayout>
        <Label Text="Welcome to .NET MAUI!"
                VerticalOptions="Center"
                HorizontalOptions="Center" />
        <!-- Other views go here -->
    </StackLayout>
</ContentPage>
```

The child of a `ContentPage` is typically a layout, such as `Grid` or `StackLayout`, with the layout typically containing multiple views. However, the child of the `ContentPage` can be a view that displays a collection, such as `CollectionView`.

> [!NOTE]
> The value of the `Title` property will be shown on the navigation bar, when the app performs navigation using a `NavigationPage`. For more information, see [NavigationPage](navigationpage.md).
