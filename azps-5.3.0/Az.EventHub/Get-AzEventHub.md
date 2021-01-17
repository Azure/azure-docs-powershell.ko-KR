---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376699"
---
# <span data-ttu-id="3d13c-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="3d13c-101">Get-AzEventHub</span></span>

## <span data-ttu-id="3d13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d13c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d13c-103">단일 이벤트 허브의 세부 정보를 얻거나 Event Hubs 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="3d13c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d13c-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d13c-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d13c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d13c-106">이 Get-AzEventHub cmdlet은 이벤트 허브의 세부 정보 또는 현재 네임스페이스의 모든 Event Hubs 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="3d13c-107">이벤트 허브 이름이 제공된 경우 단일 이벤트 허브의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="3d13c-108">이벤트 허브 이름이 제공되지 않으면 지정된 네임스페이스의 모든 Event Hubs 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="3d13c-109">예제</span><span class="sxs-lookup"><span data-stu-id="3d13c-109">EXAMPLES</span></span>

### <span data-ttu-id="3d13c-110">예제 1: 지정된 EventHub</span><span class="sxs-lookup"><span data-stu-id="3d13c-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="3d13c-111">이벤트 허브 \` MyEventHubName의 세부 정보를 \` 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="3d13c-112">예제 2: 지정된 네임스페이스의 EventHub 목록</span><span class="sxs-lookup"><span data-stu-id="3d13c-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="3d13c-113">MyNamespaceName 네임스페이스의 Event \` Hubs 목록을 \` 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="3d13c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d13c-114">PARAMETERS</span></span>

### <span data-ttu-id="3d13c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d13c-115">-DefaultProfile</span></span>
<span data-ttu-id="3d13c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d13c-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3d13c-117">-MaxCount</span></span>
<span data-ttu-id="3d13c-118">반환할 EventHubs의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d13c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d13c-119">-Name</span></span>
<span data-ttu-id="3d13c-120">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="3d13c-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d13c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d13c-121">-Namespace</span></span>
<span data-ttu-id="3d13c-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3d13c-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d13c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d13c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d13c-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3d13c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3d13c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d13c-125">CommonParameters</span></span>
<span data-ttu-id="3d13c-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d13c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d13c-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3d13c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d13c-128">입력</span><span class="sxs-lookup"><span data-stu-id="3d13c-128">INPUTS</span></span>

### <span data-ttu-id="3d13c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3d13c-129">System.String</span></span>

## <span data-ttu-id="3d13c-130">출력</span><span class="sxs-lookup"><span data-stu-id="3d13c-130">OUTPUTS</span></span>

### <span data-ttu-id="3d13c-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3d13c-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3d13c-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d13c-132">NOTES</span></span>

## <span data-ttu-id="3d13c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d13c-133">RELATED LINKS</span></span>
