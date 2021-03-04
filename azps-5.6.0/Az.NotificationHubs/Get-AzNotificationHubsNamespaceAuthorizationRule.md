---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951296"
---
# <span data-ttu-id="de763-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de763-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="de763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de763-102">SYNOPSIS</span></span>
<span data-ttu-id="de763-103">알림 허브 네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="de763-104">구문</span><span class="sxs-lookup"><span data-stu-id="de763-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de763-105">설명</span><span class="sxs-lookup"><span data-stu-id="de763-105">DESCRIPTION</span></span>
<span data-ttu-id="de763-106">**Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임스페이스와 연결된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="de763-107">네임스페이스와 연결된 모든 규칙에 대한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="de763-108">또는 *AuthorizationRule* 매개 변수를 포함하여 특정 규칙에 대한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="de763-109">권한 부여 규칙은 네임스페이스에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="de763-110">이는 서로 다른 사용 권한 수준에 따라 URIS로 링크를 만들어서 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="de763-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="de763-111">플랫폼 수준은 다음 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="de763-112">수신기</span><span class="sxs-lookup"><span data-stu-id="de763-112">Listen</span></span>
- <span data-ttu-id="de763-113">보내기</span><span class="sxs-lookup"><span data-stu-id="de763-113">Send</span></span>
- <span data-ttu-id="de763-114">클라이언트 관리는 적절한 권한 수준에 따라 이러한 URIS 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="de763-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="de763-115">예를 들어 수신 권한 부여 클라이언트는 해당 사용 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="de763-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="de763-116">이 cmdlet은 네임스페이스와 연결된 권한 부여 규칙만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="de763-117">네임스페이스 자체에 대한 정보를 얻은 경우 Get-AzNotificationHubsNamespace를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="de763-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="de763-118">예제</span><span class="sxs-lookup"><span data-stu-id="de763-118">EXAMPLES</span></span>

### <span data-ttu-id="de763-119">예제 1: 네임스페이스에 할당된 모든 권한 부여 규칙에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="de763-120">이 명령은 네임스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="de763-121">예제 2: 권한 부여 규칙에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="de763-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="de763-122">이 명령은 ListenRule이라는 단일 네임스페이스 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de763-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="de763-123">특정 권한 부여 규칙에 대한 정보를 얻을 때 네임스페이스 및 리소스 그룹을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="de763-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="de763-124">PARAMETERS</span></span>

### <span data-ttu-id="de763-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de763-125">-AuthorizationRule</span></span>
<span data-ttu-id="de763-126">SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="de763-127">이러한 규칙은 사용자가 네임스페이스에 대한 액세스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="de763-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de763-128">-DefaultProfile</span></span>
<span data-ttu-id="de763-129">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="de763-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de763-130">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="de763-130">-Namespace</span></span>
<span data-ttu-id="de763-131">권한 부여 규칙이 할당되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="de763-132">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="de763-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de763-133">-ResourceGroup</span></span>
<span data-ttu-id="de763-134">권한 부여 규칙이 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="de763-135">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="de763-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de763-136">CommonParameters</span></span>
<span data-ttu-id="de763-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="de763-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de763-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="de763-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de763-139">입력</span><span class="sxs-lookup"><span data-stu-id="de763-139">INPUTS</span></span>

### <span data-ttu-id="de763-140">System.String</span><span class="sxs-lookup"><span data-stu-id="de763-140">System.String</span></span>

## <span data-ttu-id="de763-141">출력</span><span class="sxs-lookup"><span data-stu-id="de763-141">OUTPUTS</span></span>

### <span data-ttu-id="de763-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="de763-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="de763-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="de763-143">NOTES</span></span>

## <span data-ttu-id="de763-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de763-144">RELATED LINKS</span></span>

[<span data-ttu-id="de763-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="de763-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="de763-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="de763-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="de763-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="de763-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="de763-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="de763-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


