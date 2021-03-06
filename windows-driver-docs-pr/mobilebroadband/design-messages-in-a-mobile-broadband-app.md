---
title: Design messages in a mobile broadband app
description: Design messages in a mobile broadband app
ms.assetid: 314fd479-7dcf-4559-a195-26e4c020446c
---

# Design messages in a mobile broadband app


Your mobile broadband app is a convenient way to communicate with your customers about important account information. The app should have a section or link on the home screen where end users can view important account messages. While important operator messages should be shown as tile and toast notifications, they should also be shown in app view because of the transient nature of toast notifications and the limited amount of text that can be shown in a tile notification.

You should not show user-to-user chat text messaging, promotions, and advertisements in the messages section mixed together with operator notifications and alerts because customers might miss important operator notifications. You can display promotions and advertisements in the layout of your app and display user-to-user chat text messages in a separate section of the user interface.

![message](images/message.png)

The following table shows some example operator messages and alerts.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Example message</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>International roaming</p></td>
<td><p>Welcome to the UK. For $5 per day you have 25 MB of data, and then it's $1 per 1 MB. SMS is $0.49 per msg. Learn more at www.contoso.com/rates/uk.</p></td>
</tr>
<tr class="even">
<td><p>Data usage overage</p></td>
<td><p>You’ve used your entire 4 GB data plan. Overage bills @ $10/GB. Save on more data by upgrading your plan today in the Plans page.</p></td>
</tr>
<tr class="odd">
<td><p>Data usage status</p></td>
<td><p>You’ve used 65% of your 40 GB data plan. Any overage bills @ $5/GB. Tip: Data is unlimited over Wi-Fi. Learn more in the Plans page.</p></td>
</tr>
<tr class="even">
<td><p>Plan expiration</p></td>
<td><p>Your plan expired on July 1, 2013. Renew your plan by going to the Plans page.</p></td>
</tr>
<tr class="odd">
<td><p>Account update</p></td>
<td><p>Great news! Effective immediately, Contoso is increasing the amount of data included in your DataPro Tethering plan from 2 GB to 4 GB. The monthly charge for your plan will not change and no action is required by you. Thank you for being a great customer.</p></td>
</tr>
</tbody>
</table>

 

## <span id="Quick_summary"></span><span id="quick_summary"></span><span id="QUICK_SUMMARY"></span>Quick summary


Appropriate design for showing operator messages:

-   Include functionality to view a list of all messages received, view full details of a message, and delete a message.

-   Show important operator messages in a section of the home screen of the app or on its own page in the app.

Inappropriate design for showing operator messages:

-   Don’t show user-to-user chat text messages and promotions and advertisements mixed together with operator notifications and alerts.

## <span id="Additional_resources"></span><span id="additional_resources"></span><span id="ADDITIONAL_RESOURCES"></span>Additional resources


-   Use [**ListView**](https://msdn.microsoft.com/library/windows/apps/br211837) to display messages. For more info, see [Adding List View, Semantic Zoom, and other data controls](https://msdn.microsoft.com/library/windows/apps/hh465409).

-   Use the app bar control to view and delete messages. For more info, see [Guidelines for app bars](https://msdn.microsoft.com/library/windows/apps/hh465302).

-   [Integrate a mobile broadband app with other Windows components](integrate-a-mobile-broadband-app-with-other-windows-components.md#tileandtoast)

## <span id="related_topics"></span>Related topics


[Designing the user experience of a mobile broadband app](designing-the-user-experience-of-a-mobile-broadband-app.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_mb\p_mb%5D:%20Design%20messages%20in%20a%20mobile%20broadband%20app%20%20RELEASE:%20%281/18/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





