---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336189"
---
# <span data-ttu-id="756ec-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756ec-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="756ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756ec-102">SYNOPSIS</span></span>
<span data-ttu-id="756ec-103">알림 허브에서 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="756ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="756ec-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="756ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="756ec-105">DESCRIPTION</span></span>
<span data-ttu-id="756ec-106">**Remove-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에서 SAS(공유 액세스 서명) 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="756ec-107">권한 부여 규칙은 다른 사용 권한 수준에 따라 URIS로 링크를 만들어 알림 허브에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="756ec-108">사용 권한 수준은 다음 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="756ec-109">수신</span><span class="sxs-lookup"><span data-stu-id="756ec-109">Listen</span></span>
- <span data-ttu-id="756ec-110">보내기</span><span class="sxs-lookup"><span data-stu-id="756ec-110">Send</span></span>
- <span data-ttu-id="756ec-111">관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="756ec-112">예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="756ec-113">권한 부여 규칙을 제거하면 해당 사용자 권한도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="756ec-114">예제</span><span class="sxs-lookup"><span data-stu-id="756ec-114">EXAMPLES</span></span>

### <span data-ttu-id="756ec-115">예제 1: 알림 허브에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="756ec-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="756ec-116">이 명령은 ContosoExternalHub라는 알림 허브에서 ListenRule이라는 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="756ec-117">이 명령을 실행할 때 허브가 할당된 네임스페이스와 리소스 그룹을 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="756ec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="756ec-118">PARAMETERS</span></span>

### <span data-ttu-id="756ec-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756ec-119">-AuthorizationRule</span></span>
<span data-ttu-id="756ec-120">이 cmdlet에서 제거하는 SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="756ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756ec-121">-DefaultProfile</span></span>
<span data-ttu-id="756ec-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="756ec-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="756ec-123">-Force</span><span class="sxs-lookup"><span data-stu-id="756ec-123">-Force</span></span>
<span data-ttu-id="756ec-124">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="756ec-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="756ec-125">-Namespace</span></span>
<span data-ttu-id="756ec-126">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="756ec-127">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="756ec-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="756ec-128">-NotificationHub</span></span>
<span data-ttu-id="756ec-129">권한 부여 규칙이 할당된 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="756ec-130">알림 허브는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="756ec-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="756ec-131">-ResourceGroup</span></span>
<span data-ttu-id="756ec-132">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="756ec-133">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="756ec-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="756ec-134">-Confirm</span></span>
<span data-ttu-id="756ec-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="756ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756ec-136">-WhatIf</span></span>
<span data-ttu-id="756ec-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="756ec-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="756ec-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="756ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756ec-139">CommonParameters</span></span>
<span data-ttu-id="756ec-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="756ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756ec-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="756ec-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756ec-142">입력</span><span class="sxs-lookup"><span data-stu-id="756ec-142">INPUTS</span></span>

### <span data-ttu-id="756ec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="756ec-143">System.String</span></span>

## <span data-ttu-id="756ec-144">출력</span><span class="sxs-lookup"><span data-stu-id="756ec-144">OUTPUTS</span></span>

### <span data-ttu-id="756ec-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="756ec-145">System.Void</span></span>

## <span data-ttu-id="756ec-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="756ec-146">NOTES</span></span>

## <span data-ttu-id="756ec-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="756ec-147">RELATED LINKS</span></span>

[<span data-ttu-id="756ec-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756ec-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="756ec-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756ec-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="756ec-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756ec-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


