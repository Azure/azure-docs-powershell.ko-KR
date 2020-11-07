---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: bb433499b53a1067e21996fe33fd6e9765dcab4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699915"
---
# <span data-ttu-id="46075-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="46075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46075-102">SYNOPSIS</span></span>
<span data-ttu-id="46075-103">알림 허브에 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="46075-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46075-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46075-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46075-105">DESCRIPTION</span></span>
<span data-ttu-id="46075-106">**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에 연결 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="46075-107">Cmdlet은 허브에 연결 된 모든 규칙에 대 한 정보를 반환 하 고, *Authorizationrule* 매개 변수를 포함 하 여 특정 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="46075-108">권한 부여 규칙은 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="46075-109">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 URI로 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46075-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="46075-110">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="46075-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="46075-111">예를 들어 Listen 권한이 있는 클라이언트는 해당 권한의 URI로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="46075-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="46075-112">**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에 연결 된 권한 부여 규칙에 대 한 정보만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="46075-113">허브 자체에 대 한 정보를 얻으려면 Get-help를 AzNotificationHub를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="46075-114">예제의</span><span class="sxs-lookup"><span data-stu-id="46075-114">EXAMPLES</span></span>

### <span data-ttu-id="46075-115">예제 1: 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="46075-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="46075-116">이 명령은 네임 스페이스 ContosoNamespace에서 ContosoInternalHub 이라는 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="46075-117">허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="46075-118">예제 2: 알림 허브에 할당 된 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="46075-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="46075-119">이 명령은 네임 스페이스 ContosoNamespace에서 ContosoInternalHub 이라는 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46075-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="46075-120">이 명령은 *Authorizationrule* 매개 변수를 사용 하 여 반환 된 데이터를 ListenRule 이라는 단일 인증 규칙으로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="46075-121">변수</span><span class="sxs-lookup"><span data-stu-id="46075-121">PARAMETERS</span></span>

### <span data-ttu-id="46075-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-122">-AuthorizationRule</span></span>
<span data-ttu-id="46075-123">SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="46075-124">이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="46075-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46075-125">-DefaultProfile</span></span>
<span data-ttu-id="46075-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46075-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46075-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46075-127">-Namespace</span></span>
<span data-ttu-id="46075-128">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="46075-129">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="46075-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="46075-130">-NotificationHub</span></span>
<span data-ttu-id="46075-131">이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="46075-132">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46075-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="46075-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46075-133">-ResourceGroup</span></span>
<span data-ttu-id="46075-134">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="46075-135">리소스 그룹은 인벤토리 관리 및 Azure 관리를 간소화 하는 데 도움이 되는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="46075-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46075-136">CommonParameters</span></span>
<span data-ttu-id="46075-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46075-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46075-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46075-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46075-139">입력</span><span class="sxs-lookup"><span data-stu-id="46075-139">INPUTS</span></span>

### <span data-ttu-id="46075-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46075-140">System.String</span></span>

## <span data-ttu-id="46075-141">출력</span><span class="sxs-lookup"><span data-stu-id="46075-141">OUTPUTS</span></span>

### <span data-ttu-id="46075-142">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="46075-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="46075-143">상속자</span><span class="sxs-lookup"><span data-stu-id="46075-143">NOTES</span></span>

## <span data-ttu-id="46075-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46075-144">RELATED LINKS</span></span>

[<span data-ttu-id="46075-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="46075-146">새로운 AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="46075-147">제거-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="46075-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46075-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


