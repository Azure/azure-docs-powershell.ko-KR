---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: c3740884d49683b7990aea1ed7543f39a4ccf80f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872518"
---
# <span data-ttu-id="8dab1-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8dab1-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="8dab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dab1-102">SYNOPSIS</span></span>
<span data-ttu-id="8dab1-103">기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="8dab1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dab1-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dab1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8dab1-105">DESCRIPTION</span></span>
<span data-ttu-id="8dab1-106">**AzNotificationHub** cmdlet에서는 기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="8dab1-107">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="8dab1-108">플랫폼에는 iOS, Android, Windows Phone 8, Windows 스토어가 포함 되지만이에 국한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="8dab1-109">알림 허브는 개별 앱과 거의 동일 합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="8dab1-110">**제거-AzNotificationHub** cmdlet을 사용 하 여 기존 알림 허브를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="8dab1-111">허브가 제거 된 후에는 더 이상 해당 허브를 사용 하 여 사용자에 게 푸시 알림을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="8dab1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8dab1-112">EXAMPLES</span></span>

### <span data-ttu-id="8dab1-113">예제 1: 알림 허브 제거</span><span class="sxs-lookup"><span data-stu-id="8dab1-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8dab1-114">이 명령은 ContosoInternalHub 이라는 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="8dab1-115">허브를 제거 하려면 허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="8dab1-116">변수</span><span class="sxs-lookup"><span data-stu-id="8dab1-116">PARAMETERS</span></span>

### <span data-ttu-id="8dab1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dab1-117">-DefaultProfile</span></span>
<span data-ttu-id="8dab1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8dab1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dab1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8dab1-119">-Force</span></span>
<span data-ttu-id="8dab1-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8dab1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8dab1-121">-Namespace</span></span>
<span data-ttu-id="8dab1-122">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8dab1-123">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8dab1-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8dab1-124">-NotificationHub</span></span>
<span data-ttu-id="8dab1-125">제거할 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="8dab1-126">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8dab1-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8dab1-127">-ResourceGroup</span></span>
<span data-ttu-id="8dab1-128">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8dab1-129">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8dab1-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8dab1-130">-Confirm</span></span>
<span data-ttu-id="8dab1-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dab1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dab1-132">-WhatIf</span></span>
<span data-ttu-id="8dab1-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dab1-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dab1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dab1-135">CommonParameters</span></span>
<span data-ttu-id="8dab1-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dab1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dab1-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dab1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dab1-138">입력</span><span class="sxs-lookup"><span data-stu-id="8dab1-138">INPUTS</span></span>

### <span data-ttu-id="8dab1-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dab1-139">System.String</span></span>

## <span data-ttu-id="8dab1-140">출력</span><span class="sxs-lookup"><span data-stu-id="8dab1-140">OUTPUTS</span></span>

### <span data-ttu-id="8dab1-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="8dab1-141">System.Void</span></span>

## <span data-ttu-id="8dab1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8dab1-142">NOTES</span></span>

## <span data-ttu-id="8dab1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dab1-143">RELATED LINKS</span></span>

[<span data-ttu-id="8dab1-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8dab1-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="8dab1-145">새로운 AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8dab1-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="8dab1-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8dab1-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


