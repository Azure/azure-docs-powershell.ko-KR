---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385078"
---
# <span data-ttu-id="f94c7-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f94c7-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f94c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f94c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f94c7-103">알림 허브 네임스페이스에서 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="f94c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="f94c7-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f94c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="f94c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f94c7-106">**Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임스페이스에서 SAS(공유 액세스 서명) 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="f94c7-107">권한 부여 규칙은 네임스페이스에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="f94c7-108">이는 다른 사용 권한 수준에 따라 URIS로 링크를 만들어 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f94c7-109">사용 권한 수준은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="f94c7-110">수신</span><span class="sxs-lookup"><span data-stu-id="f94c7-110">Listen</span></span>
- <span data-ttu-id="f94c7-111">보내기</span><span class="sxs-lookup"><span data-stu-id="f94c7-111">Send</span></span>
- <span data-ttu-id="f94c7-112">관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f94c7-113">예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="f94c7-114">권한 부여 규칙을 제거하면 해당 사용자 권한도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="f94c7-115">예제</span><span class="sxs-lookup"><span data-stu-id="f94c7-115">EXAMPLES</span></span>

### <span data-ttu-id="f94c7-116">예제 1: 네임스페이스에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="f94c7-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f94c7-117">이 명령은 ContosoNamespace라는 네임스페이스에서 ListenRule이라는 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="f94c7-118">이 명령을 실행할 때 네임스페이스가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="f94c7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f94c7-119">PARAMETERS</span></span>

### <span data-ttu-id="f94c7-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f94c7-120">-AuthorizationRule</span></span>
<span data-ttu-id="f94c7-121">제거할 SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="f94c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94c7-122">-DefaultProfile</span></span>
<span data-ttu-id="f94c7-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f94c7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f94c7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f94c7-124">-Force</span></span>
<span data-ttu-id="f94c7-125">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f94c7-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f94c7-126">-Namespace</span></span>
<span data-ttu-id="f94c7-127">권한 부여 규칙이 할당되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f94c7-128">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f94c7-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f94c7-129">-ResourceGroup</span></span>
<span data-ttu-id="f94c7-130">네임스페이스가 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="f94c7-131">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f94c7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f94c7-132">-Confirm</span></span>
<span data-ttu-id="f94c7-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94c7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94c7-134">-WhatIf</span></span>
<span data-ttu-id="f94c7-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f94c7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f94c7-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94c7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94c7-137">CommonParameters</span></span>
<span data-ttu-id="f94c7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f94c7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94c7-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f94c7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94c7-140">입력</span><span class="sxs-lookup"><span data-stu-id="f94c7-140">INPUTS</span></span>

### <span data-ttu-id="f94c7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f94c7-141">System.String</span></span>

## <span data-ttu-id="f94c7-142">출력</span><span class="sxs-lookup"><span data-stu-id="f94c7-142">OUTPUTS</span></span>

### <span data-ttu-id="f94c7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f94c7-143">System.Boolean</span></span>

## <span data-ttu-id="f94c7-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f94c7-144">NOTES</span></span>

## <span data-ttu-id="f94c7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f94c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="f94c7-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f94c7-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f94c7-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f94c7-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f94c7-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f94c7-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


