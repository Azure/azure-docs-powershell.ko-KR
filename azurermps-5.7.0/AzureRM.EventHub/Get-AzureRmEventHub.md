---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529833"
---
# <span data-ttu-id="e8744-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="e8744-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="e8744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8744-102">SYNOPSIS</span></span>
<span data-ttu-id="e8744-103">단일 이벤트 허브의 세부 정보를 가져오거나 이벤트 허브 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8744-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8744-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8744-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8744-105">DESCRIPTION</span></span>
<span data-ttu-id="e8744-106">Get-AzureRmEventHub cmdlet은 이벤트 허브의 세부 정보 또는 현재 네임 스페이스에 있는 모든 이벤트 허브의 목록 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="e8744-107">이벤트 허브 이름을 제공 하는 경우 단일 이벤트 허브에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="e8744-108">이벤트 허브 이름을 제공 하지 않으면 지정 된 네임 스페이스에 있는 모든 이벤트 허브 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="e8744-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e8744-109">EXAMPLES</span></span>

### <span data-ttu-id="e8744-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8744-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e8744-111">이벤트 허브 MyEventHubName의 세부 정보를 반환 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="e8744-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="e8744-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e8744-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e8744-113">네임 스페이스 MyNamespaceName의 이벤트 허브 목록을 반환 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e8744-114">변수</span><span class="sxs-lookup"><span data-stu-id="e8744-114">PARAMETERS</span></span>

### <span data-ttu-id="e8744-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8744-115">-DefaultProfile</span></span>
<span data-ttu-id="e8744-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8744-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e8744-117">-Name</span></span>
<span data-ttu-id="e8744-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="e8744-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8744-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8744-119">-Namespace</span></span>
<span data-ttu-id="e8744-120">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e8744-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8744-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8744-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8744-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e8744-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e8744-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8744-123">CommonParameters</span></span>
<span data-ttu-id="e8744-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8744-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e8744-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8744-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8744-126">입력</span><span class="sxs-lookup"><span data-stu-id="e8744-126">INPUTS</span></span>

### <span data-ttu-id="e8744-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8744-127">System.String</span></span>


## <span data-ttu-id="e8744-128">출력</span><span class="sxs-lookup"><span data-stu-id="e8744-128">OUTPUTS</span></span>

### <span data-ttu-id="e8744-129">System.webserver. List ' 1 [[Microsoft PSEventHubAttributes, Microsoft Azure. 0.5.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="e8744-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e8744-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e8744-130">NOTES</span></span>

## <span data-ttu-id="e8744-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8744-131">RELATED LINKS</span></span>
