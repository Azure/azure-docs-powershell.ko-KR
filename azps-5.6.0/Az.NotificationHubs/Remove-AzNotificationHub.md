---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: b7932eb4f5d68986033243bc3e5e5161861a0bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951152"
---
# <span data-ttu-id="992a7-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="992a7-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="992a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992a7-102">SYNOPSIS</span></span>
<span data-ttu-id="992a7-103">기존 알림 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="992a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="992a7-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="992a7-105">설명</span><span class="sxs-lookup"><span data-stu-id="992a7-105">DESCRIPTION</span></span>
<span data-ttu-id="992a7-106">**Remove-AzNotificationHub** cmdlet은 기존 알림 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="992a7-107">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="992a7-108">플랫폼에는 iOS, Android, Windows Phone 8 및 Windows Store가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="992a7-109">알림 허브는 개별 앱과 거의 동일합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="992a7-110">**Remove-AzNotificationHub** cmdlet을 사용하여 기존 알림 허브를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="992a7-111">허브가 제거된 후 해당 허브를 사용하여 사용자에게 푸시 알림을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="992a7-112">예제</span><span class="sxs-lookup"><span data-stu-id="992a7-112">EXAMPLES</span></span>

### <span data-ttu-id="992a7-113">예제 1: 알림 허브 제거</span><span class="sxs-lookup"><span data-stu-id="992a7-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="992a7-114">이 명령은 ContosoInternalHub라는 알림 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="992a7-115">허브를 제거하려면 허브가 있는 네임스페이스와 허브가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="992a7-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="992a7-116">PARAMETERS</span></span>

### <span data-ttu-id="992a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992a7-117">-DefaultProfile</span></span>
<span data-ttu-id="992a7-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="992a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="992a7-119">-Force</span></span>
<span data-ttu-id="992a7-120">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-120">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="992a7-121">-Namespace</span></span>
<span data-ttu-id="992a7-122">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="992a7-123">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="992a7-124">-NotificationHub</span></span>
<span data-ttu-id="992a7-125">제거할 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="992a7-126">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="992a7-127">-ResourceGroup</span></span>
<span data-ttu-id="992a7-128">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="992a7-129">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="992a7-130">-Confirm</span></span>
<span data-ttu-id="992a7-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992a7-132">-WhatIf</span></span>
<span data-ttu-id="992a7-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="992a7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992a7-135">CommonParameters</span></span>
<span data-ttu-id="992a7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="992a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992a7-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="992a7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992a7-138">입력</span><span class="sxs-lookup"><span data-stu-id="992a7-138">INPUTS</span></span>

### <span data-ttu-id="992a7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="992a7-139">System.String</span></span>

## <span data-ttu-id="992a7-140">출력</span><span class="sxs-lookup"><span data-stu-id="992a7-140">OUTPUTS</span></span>

### <span data-ttu-id="992a7-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="992a7-141">System.Void</span></span>

## <span data-ttu-id="992a7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="992a7-142">NOTES</span></span>

## <span data-ttu-id="992a7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="992a7-143">RELATED LINKS</span></span>

[<span data-ttu-id="992a7-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="992a7-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="992a7-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="992a7-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="992a7-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="992a7-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


