---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191532"
---
# <span data-ttu-id="9fc3f-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="9fc3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc3f-103">알림 허브와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="9fc3f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9fc3f-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc3f-105">설명</span><span class="sxs-lookup"><span data-stu-id="9fc3f-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc3f-106">**Get-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브와 연결된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="9fc3f-107">cmdlet은 허브와 연결된 모든 규칙에 대한 정보를 반환하거나 *AuthorizationRule* 매개 변수를 포함하여 특정 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="9fc3f-108">권한 부여 규칙은 알림 허브에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="9fc3f-109">권한 부여 규칙은 다른 사용 권한 수준에 따라 URI로 링크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="9fc3f-110">클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9fc3f-111">예를 들어 수신 권한이 있는 클라이언트는 해당 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="9fc3f-112">**Get-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브와 연결된 권한 부여 규칙에 대한 정보만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="9fc3f-113">허브 자체에 대한 정보를 얻습니다. Get-AzNotificationHub를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="9fc3f-114">예제</span><span class="sxs-lookup"><span data-stu-id="9fc3f-114">EXAMPLES</span></span>

### <span data-ttu-id="9fc3f-115">예제 1: 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="9fc3f-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="9fc3f-116">이 명령은 ContosoNamespace 네임스페이스에서 ContosoInternalHub라는 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="9fc3f-117">허브가 있는 네임스페이스와 허브가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="9fc3f-118">예제 2: 알림 허브에 할당된 권한 부여 규칙에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="9fc3f-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9fc3f-119">이 명령은 ContosoNamespace 네임스페이스에서 ContosoInternalHub라는 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="9fc3f-120">이 명령은 *AuthorizationRule* 매개 변수를 사용하여 반환된 데이터를 ListenRule이라는 단일 권한 부여 규칙으로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="9fc3f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fc3f-121">PARAMETERS</span></span>

### <span data-ttu-id="9fc3f-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-122">-AuthorizationRule</span></span>
<span data-ttu-id="9fc3f-123">SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="9fc3f-124">이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc3f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc3f-125">-DefaultProfile</span></span>
<span data-ttu-id="9fc3f-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9fc3f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fc3f-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9fc3f-127">-Namespace</span></span>
<span data-ttu-id="9fc3f-128">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9fc3f-129">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9fc3f-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9fc3f-130">-NotificationHub</span></span>
<span data-ttu-id="9fc3f-131">이 cmdlet이 권한 부여 규칙을 할당하는 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="9fc3f-132">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="9fc3f-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9fc3f-133">-ResourceGroup</span></span>
<span data-ttu-id="9fc3f-134">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9fc3f-135">리소스 그룹은 인벤토리 관리 및 Azure 관리를 간소화하는 데 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9fc3f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc3f-136">CommonParameters</span></span>
<span data-ttu-id="9fc3f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc3f-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9fc3f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc3f-139">입력</span><span class="sxs-lookup"><span data-stu-id="9fc3f-139">INPUTS</span></span>

### <span data-ttu-id="9fc3f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9fc3f-140">System.String</span></span>

## <span data-ttu-id="9fc3f-141">출력</span><span class="sxs-lookup"><span data-stu-id="9fc3f-141">OUTPUTS</span></span>

### <span data-ttu-id="9fc3f-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9fc3f-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9fc3f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9fc3f-143">NOTES</span></span>

## <span data-ttu-id="9fc3f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fc3f-144">RELATED LINKS</span></span>

[<span data-ttu-id="9fc3f-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="9fc3f-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9fc3f-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="9fc3f-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fc3f-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


