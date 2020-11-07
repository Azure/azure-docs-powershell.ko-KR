---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 6ad682ad80400fa84034b35804c9756775d05eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699885"
---
# <span data-ttu-id="95a3f-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95a3f-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="95a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="95a3f-103">알림 허브에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="95a3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95a3f-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="95a3f-106">**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에서 SAS (공유 액세스 서명) 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="95a3f-107">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="95a3f-108">사용 권한 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="95a3f-109">듣기</span><span class="sxs-lookup"><span data-stu-id="95a3f-109">Listen</span></span>
- <span data-ttu-id="95a3f-110">보내기</span><span class="sxs-lookup"><span data-stu-id="95a3f-110">Send</span></span>
- <span data-ttu-id="95a3f-111">클라이언트 관리는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 향합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="95a3f-112">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="95a3f-113">권한 부여 규칙을 제거 하면 해당 사용자 권한도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="95a3f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="95a3f-114">EXAMPLES</span></span>

### <span data-ttu-id="95a3f-115">예제 1: 알림 허브에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="95a3f-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="95a3f-116">이 명령은 ContosoExternalHub 이라는 알림 허브에서 ListenRule 이라는 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="95a3f-117">이 명령을 실행할 때는 네임 스페이스와 허브가 할당 된 리소스 그룹을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="95a3f-118">변수</span><span class="sxs-lookup"><span data-stu-id="95a3f-118">PARAMETERS</span></span>

### <span data-ttu-id="95a3f-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95a3f-119">-AuthorizationRule</span></span>
<span data-ttu-id="95a3f-120">이 cmdlet이 제거 하는 SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95a3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a3f-121">-DefaultProfile</span></span>
<span data-ttu-id="95a3f-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95a3f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95a3f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="95a3f-123">-Force</span></span>
<span data-ttu-id="95a3f-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="95a3f-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95a3f-125">-Namespace</span></span>
<span data-ttu-id="95a3f-126">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="95a3f-127">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="95a3f-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="95a3f-128">-NotificationHub</span></span>
<span data-ttu-id="95a3f-129">권한 부여 규칙이 할당 되는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="95a3f-130">알림 허브는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="95a3f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95a3f-131">-ResourceGroup</span></span>
<span data-ttu-id="95a3f-132">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="95a3f-133">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="95a3f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="95a3f-134">-Confirm</span></span>
<span data-ttu-id="95a3f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a3f-136">-WhatIf</span></span>
<span data-ttu-id="95a3f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95a3f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a3f-139">CommonParameters</span></span>
<span data-ttu-id="95a3f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a3f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a3f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a3f-142">입력</span><span class="sxs-lookup"><span data-stu-id="95a3f-142">INPUTS</span></span>

### <span data-ttu-id="95a3f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95a3f-143">System.String</span></span>

## <span data-ttu-id="95a3f-144">출력</span><span class="sxs-lookup"><span data-stu-id="95a3f-144">OUTPUTS</span></span>

### <span data-ttu-id="95a3f-145">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="95a3f-145">System.Void</span></span>

## <span data-ttu-id="95a3f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="95a3f-146">NOTES</span></span>

## <span data-ttu-id="95a3f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95a3f-147">RELATED LINKS</span></span>

[<span data-ttu-id="95a3f-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95a3f-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="95a3f-149">새로운 AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95a3f-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="95a3f-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95a3f-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


