---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529251"
---
# <span data-ttu-id="78219-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="78219-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="78219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78219-102">SYNOPSIS</span></span>
<span data-ttu-id="78219-103">알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78219-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78219-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78219-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78219-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78219-105">DESCRIPTION</span></span>
<span data-ttu-id="78219-106">**AzureRmNotificationHubsNamespace Cmdlet은** 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78219-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="78219-107">이 cmdlet은 모든 네임 스페이스, 즉 지정 된 리소스 그룹에 할당 된 네임 스페이스에 대 한 정보를 가져올 수 있는 옵션을 제공 합니다. 특정 네임 스페이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="78219-108">네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="78219-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="78219-109">하나 이상의 알림 허브 네임 스페이스가 있어야 합니다. 모든 알림 허브는 네임 스페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="78219-110">단일 네임 스페이스는 조직에서 하나의 네임 스페이스만 필요할 수 있다는 것을 의미 하는 여러 허브를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78219-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="78219-111">그러나 허브를 더 효과적으로 구성 하거나 특정 개인에 게 선택한 허브 하위 집합을 관리할 수 있는 권한을 부여 하기 위해 여러 네임 스페이스를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78219-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="78219-112">**Get-AzureRmNotificationHubsNamespace** cmdlet은 네임 스페이스 자체에 대 한 기본 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="78219-113">네임 스페이스에 연결 된 권한 부여 규칙에 대 한 정보를 얻으려면 Get-AzureRmNotificationHubsNamespaceAuthorizationRules를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="78219-114">예제의</span><span class="sxs-lookup"><span data-stu-id="78219-114">EXAMPLES</span></span>

### <span data-ttu-id="78219-115">예제 1: 모든 알림 허브 네임 스페이스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="78219-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="78219-116">이 명령은 모든 알림 허브 네임 스페이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="78219-117">예제 2: 단일 알림 허브 네임 스페이스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="78219-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="78219-118">이 명령은 단일 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="78219-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="78219-119">예제 3: 특정 네임 스페이스에 할당 된 모든 알림 허브에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="78219-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="78219-120">이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 모든 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78219-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="78219-121">변수</span><span class="sxs-lookup"><span data-stu-id="78219-121">PARAMETERS</span></span>

### <span data-ttu-id="78219-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="78219-122">-Namespace</span></span>
<span data-ttu-id="78219-123">네임 스페이스에 대 한 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-123">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="78219-124">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="78219-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78219-125">-ResourceGroup</span></span>
<span data-ttu-id="78219-126">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-126">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="78219-127">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="78219-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78219-128">-DefaultProfile</span></span>
<span data-ttu-id="78219-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78219-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78219-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78219-130">CommonParameters</span></span>
<span data-ttu-id="78219-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78219-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78219-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78219-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78219-133">입력</span><span class="sxs-lookup"><span data-stu-id="78219-133">INPUTS</span></span>

## <span data-ttu-id="78219-134">출력</span><span class="sxs-lookup"><span data-stu-id="78219-134">OUTPUTS</span></span>

### <span data-ttu-id="78219-135">NamespaceAttributes의 목록 ' 1 [Microsoft. h t e.]</span><span class="sxs-lookup"><span data-stu-id="78219-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="78219-136">상속자</span><span class="sxs-lookup"><span data-stu-id="78219-136">NOTES</span></span>

## <span data-ttu-id="78219-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78219-137">RELATED LINKS</span></span>

[<span data-ttu-id="78219-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="78219-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="78219-139">새로운 AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="78219-139">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="78219-140">제거-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="78219-140">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="78219-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="78219-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)

