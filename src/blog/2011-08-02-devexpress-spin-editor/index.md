---
title: "Using DevExpress ASP.Net Spin Editor Control"
description: "Summary or brief description of the post to be displayed"
date: 2011-08-02
tags: 
    - development
    - code
    - c#
---

{% image "./jeremy-zero-Vu2R3PqstrU-unsplash.jpg", "Shows windows computer destop with a software installation window" %}

The DevExpress ASP.Net spin editor control is one of those simple but extremely useful controls. I tend to use this control a lot in my projects. It basically is a text input field which only allows the user to enter numeric data.
I know on the face of it does not seem revolutionary, but a few things I like about the control are:

<!--more-->

1. Small and large increment buttons
2. Control features can be setup through markup
3. Control value can be retrieved as either a string or int/decimal value (this saves writing code that casts to a string or int/decimal)

Below is the markup for the spin edit control.

```
<dx:ASPxSpinEdit ID="dxspinAmount" runat="server" Height="21px" Number="0" NumberType="Integer" Increment="2" AllowNull="false" Enabled="false" >
    <SpinButtons Position="Left" ShowLargeIncrementButtons="true"></SpinButtons>
</dx:ASPxSpinEdit>
```

{% image "./spinedit.png", "ASP.Net Spin Editor Control" %}