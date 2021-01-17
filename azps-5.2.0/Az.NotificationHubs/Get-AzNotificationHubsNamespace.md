---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336249"
---
# <span data-ttu-id="31958-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31958-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="31958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31958-102">SYNOPSIS</span></span>
<span data-ttu-id="31958-103">알림 허브 네임스페이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="31958-104">구문</span><span class="sxs-lookup"><span data-stu-id="31958-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31958-105">설명</span><span class="sxs-lookup"><span data-stu-id="31958-105">DESCRIPTION</span></span>
<span data-ttu-id="31958-106">**Get-AzNotificationHubsNamespace** cmdlet은 알림 허브 네임스페이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="31958-107">이 cmdlet은 모든 네임스페이스에 대한 정보, 지정된 리소스 그룹에 할당된 네임스페이스에 대한 정보를 제공하는 옵션을 제공합니다. 또는 특정 네임스페이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="31958-108">네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="31958-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="31958-109">알림 허브 네임스페이스가 하나 이상 있어야 합니다. 모든 알림 허브를 네임스페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="31958-110">단일 네임스페이스는 여러 허브를 사용할 수 있습니다. 즉, 조직에 하나의 네임스페이스만 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="31958-111">그러나 허브를 보다 효율적으로 구성하거나 특정 개인에게 선택한 허브 하위 집합을 관리할 수 있는 권한을 부여하기 위해 여러 네임스페이스를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="31958-112">**Get-AzNotificationHubsNamespace** cmdlet은 네임스페이스 자체에 대한 기본 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="31958-113">네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다. Get-AzNotificationHubsNamespaceAuthorizationRules를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="31958-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="31958-114">예제</span><span class="sxs-lookup"><span data-stu-id="31958-114">EXAMPLES</span></span>

### <span data-ttu-id="31958-115">예제 1: 모든 알림 허브 네임스페이스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="31958-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="31958-116">이 명령은 모든 알림 허브 네임스페이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="31958-117">예제 2: 단일 알림 허브 네임스페이스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="31958-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="31958-118">이 명령은 단일 알림 허브 네임스페이스인 ContosoNamespace에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="31958-119">예제 3: 특정 네임스페이스에 할당된 모든 알림 허브에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="31958-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="31958-120">이 명령은 리소스 그룹에 할당된 모든 알림 허브 네임스페이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31958-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="31958-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31958-121">PARAMETERS</span></span>

### <span data-ttu-id="31958-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31958-122">-DefaultProfile</span></span>
<span data-ttu-id="31958-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31958-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31958-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="31958-124">-Namespace</span></span>
<span data-ttu-id="31958-125">네임스페이스에 대한 고유한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="31958-126">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="31958-127">-ResourceGroup</span></span>
<span data-ttu-id="31958-128">네임스페이스가 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="31958-129">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31958-130">CommonParameters</span></span>
<span data-ttu-id="31958-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31958-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31958-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31958-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31958-133">입력</span><span class="sxs-lookup"><span data-stu-id="31958-133">INPUTS</span></span>

### <span data-ttu-id="31958-134">System.String</span><span class="sxs-lookup"><span data-stu-id="31958-134">System.String</span></span>

## <span data-ttu-id="31958-135">출력</span><span class="sxs-lookup"><span data-stu-id="31958-135">OUTPUTS</span></span>

### <span data-ttu-id="31958-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="31958-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="31958-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31958-137">NOTES</span></span>

## <span data-ttu-id="31958-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31958-138">RELATED LINKS</span></span>

[<span data-ttu-id="31958-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="31958-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="31958-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31958-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="31958-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31958-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="31958-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31958-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


