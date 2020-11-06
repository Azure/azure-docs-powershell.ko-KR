---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537272"
---
# <span data-ttu-id="8538f-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="8538f-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="8538f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8538f-102">SYNOPSIS</span></span>
<span data-ttu-id="8538f-103">단일 이벤트 허브의 세부 정보를 가져오거나 이벤트 허브 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8538f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8538f-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="8538f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8538f-105">DESCRIPTION</span></span>
<span data-ttu-id="8538f-106">Get-AzureRmEventHub cmdlet은 이벤트 허브의 세부 정보 또는 현재 네임 스페이스에 있는 모든 이벤트 허브의 목록 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="8538f-107">이벤트 허브 이름을 제공 하는 경우 단일 이벤트 허브에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="8538f-108">이벤트 허브 이름을 제공 하지 않으면 지정 된 네임 스페이스에 있는 모든 이벤트 허브 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="8538f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8538f-109">EXAMPLES</span></span>

### <span data-ttu-id="8538f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8538f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8538f-111">이벤트 허브 MyEventHubName의 세부 정보를 반환 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8538f-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="8538f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8538f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="8538f-113">네임 스페이스 MyNamespaceName의 이벤트 허브 목록을 반환 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8538f-114">변수</span><span class="sxs-lookup"><span data-stu-id="8538f-114">PARAMETERS</span></span>

### <span data-ttu-id="8538f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8538f-115">-ResourceGroupName</span></span>
<span data-ttu-id="8538f-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8538f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8538f-117">-Name</span></span>
<span data-ttu-id="8538f-118">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="8538f-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8538f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8538f-119">-Namespace</span></span>
<span data-ttu-id="8538f-120">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8538f-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="8538f-121">입력</span><span class="sxs-lookup"><span data-stu-id="8538f-121">INPUTS</span></span>

### <span data-ttu-id="8538f-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8538f-122">System.String</span></span>

## <span data-ttu-id="8538f-123">출력</span><span class="sxs-lookup"><span data-stu-id="8538f-123">OUTPUTS</span></span>

### <span data-ttu-id="8538f-124">System.webserver. List ' 1 [[Microsoft EventHubAttributes, Microsoft Azure. 0.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="8538f-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8538f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8538f-125">NOTES</span></span>

## <span data-ttu-id="8538f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8538f-126">RELATED LINKS</span></span>

