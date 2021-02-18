---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206424"
---
# <span data-ttu-id="073ba-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="073ba-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="073ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073ba-102">SYNOPSIS</span></span>
<span data-ttu-id="073ba-103">알림 허브 네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="073ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="073ba-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="073ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="073ba-105">DESCRIPTION</span></span>
<span data-ttu-id="073ba-106">**Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임스페이스와 연결된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="073ba-107">네임스페이스와 연결된 모든 규칙에 대한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="073ba-108">또는 *AuthorizationRule* 매개 변수를 포함하면 특정 규칙에 대한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="073ba-109">권한 부여 규칙은 네임스페이스에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="073ba-110">이는 다른 사용 권한 수준에 따라 URIS로 링크를 만들어서 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="073ba-111">플랫폼 수준은 다음 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="073ba-112">수신</span><span class="sxs-lookup"><span data-stu-id="073ba-112">Listen</span></span>
- <span data-ttu-id="073ba-113">보내기</span><span class="sxs-lookup"><span data-stu-id="073ba-113">Send</span></span>
- <span data-ttu-id="073ba-114">관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="073ba-115">예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="073ba-116">이 cmdlet은 네임스페이스와 연결된 권한 부여 규칙만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="073ba-117">네임스페이스 자체에 대한 정보를 얻습니다. Get-AzNotificationHubsNamespace를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="073ba-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="073ba-118">예제</span><span class="sxs-lookup"><span data-stu-id="073ba-118">EXAMPLES</span></span>

### <span data-ttu-id="073ba-119">예제 1: 네임스페이스에 할당된 모든 권한 부여 규칙에 대한 정보</span><span class="sxs-lookup"><span data-stu-id="073ba-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="073ba-120">이 명령은 네임스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="073ba-121">예제 2: 권한 부여 규칙에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="073ba-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="073ba-122">이 명령은 ListenRule이라는 단일 네임스페이스 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="073ba-123">특정 권한 부여 규칙에 대한 정보를 얻을 때 네임스페이스 및 리소스 그룹을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="073ba-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="073ba-124">PARAMETERS</span></span>

### <span data-ttu-id="073ba-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="073ba-125">-AuthorizationRule</span></span>
<span data-ttu-id="073ba-126">SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="073ba-127">이러한 규칙은 사용자가 네임스페이스에 대한 액세스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="073ba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073ba-128">-DefaultProfile</span></span>
<span data-ttu-id="073ba-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="073ba-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="073ba-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="073ba-130">-Namespace</span></span>
<span data-ttu-id="073ba-131">권한 부여 규칙이 할당되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="073ba-132">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="073ba-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="073ba-133">-ResourceGroup</span></span>
<span data-ttu-id="073ba-134">권한 부여 규칙이 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="073ba-135">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="073ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073ba-136">CommonParameters</span></span>
<span data-ttu-id="073ba-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="073ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073ba-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="073ba-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073ba-139">입력</span><span class="sxs-lookup"><span data-stu-id="073ba-139">INPUTS</span></span>

### <span data-ttu-id="073ba-140">System.String</span><span class="sxs-lookup"><span data-stu-id="073ba-140">System.String</span></span>

## <span data-ttu-id="073ba-141">출력</span><span class="sxs-lookup"><span data-stu-id="073ba-141">OUTPUTS</span></span>

### <span data-ttu-id="073ba-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="073ba-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="073ba-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="073ba-143">NOTES</span></span>

## <span data-ttu-id="073ba-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="073ba-144">RELATED LINKS</span></span>

[<span data-ttu-id="073ba-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="073ba-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="073ba-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="073ba-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="073ba-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="073ba-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="073ba-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="073ba-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


