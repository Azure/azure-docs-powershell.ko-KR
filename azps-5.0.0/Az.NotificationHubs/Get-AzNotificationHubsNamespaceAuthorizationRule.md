---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309119"
---
# <span data-ttu-id="4f3a4-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4f3a4-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4f3a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3a4-103">알림 허브 네임 스페이스와 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="4f3a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f3a4-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f3a4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f3a4-105">DESCRIPTION</span></span>
<span data-ttu-id="4f3a4-106">**AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임 스페이스와 관련 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="4f3a4-107">네임 스페이스와 관련 된 모든 규칙에 대 한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="4f3a4-108">또는 *authorizationrule* 매개 변수를 포함 하 여 특정 규칙에 대 한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="4f3a4-109">권한 부여 규칙은 네임 스페이스에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="4f3a4-110">이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="4f3a4-111">플랫폼 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="4f3a4-112">듣기</span><span class="sxs-lookup"><span data-stu-id="4f3a4-112">Listen</span></span>
- <span data-ttu-id="4f3a4-113">보내기</span><span class="sxs-lookup"><span data-stu-id="4f3a4-113">Send</span></span>
- <span data-ttu-id="4f3a4-114">클라이언트 관리는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 향합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="4f3a4-115">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="4f3a4-116">이 cmdlet은 네임 스페이스와 관련 된 권한 부여 규칙만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="4f3a4-117">네임 스페이스 자체에 대 한 정보를 얻으려면 Get-AzNotificationHubsNamespace를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="4f3a4-118">예제의</span><span class="sxs-lookup"><span data-stu-id="4f3a4-118">EXAMPLES</span></span>

### <span data-ttu-id="4f3a4-119">예제 1: 네임 스페이스에 할당 된 모든 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3a4-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="4f3a4-120">이 명령은 네임 스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 모두 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="4f3a4-121">예제 2: 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3a4-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="4f3a4-122">이 명령은 ListenRule 이라는 단일 네임 스페이스 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="4f3a4-123">특정 권한 부여 규칙에 대 한 정보를 가져올 때는 네임 스페이스와 리소스 그룹을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="4f3a4-124">변수</span><span class="sxs-lookup"><span data-stu-id="4f3a4-124">PARAMETERS</span></span>

### <span data-ttu-id="4f3a4-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4f3a4-125">-AuthorizationRule</span></span>
<span data-ttu-id="4f3a4-126">SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="4f3a4-127">이러한 규칙은 네임 스페이스에 대 한 사용자의 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="4f3a4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3a4-128">-DefaultProfile</span></span>
<span data-ttu-id="4f3a4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f3a4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f3a4-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4f3a4-130">-Namespace</span></span>
<span data-ttu-id="4f3a4-131">권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="4f3a4-132">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4f3a4-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f3a4-133">-ResourceGroup</span></span>
<span data-ttu-id="4f3a4-134">권한 부여 규칙이 할당 되는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="4f3a4-135">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4f3a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3a4-136">CommonParameters</span></span>
<span data-ttu-id="4f3a4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3a4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3a4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3a4-139">입력</span><span class="sxs-lookup"><span data-stu-id="4f3a4-139">INPUTS</span></span>

### <span data-ttu-id="4f3a4-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f3a4-140">System.String</span></span>

## <span data-ttu-id="4f3a4-141">출력</span><span class="sxs-lookup"><span data-stu-id="4f3a4-141">OUTPUTS</span></span>

### <span data-ttu-id="4f3a4-142">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4f3a4-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4f3a4-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4f3a4-143">NOTES</span></span>

## <span data-ttu-id="4f3a4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f3a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f3a4-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="4f3a4-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="4f3a4-146">새로운 AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="4f3a4-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="4f3a4-147">제거-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="4f3a4-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="4f3a4-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="4f3a4-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


