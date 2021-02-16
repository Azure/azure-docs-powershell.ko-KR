---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194417"
---
# <span data-ttu-id="83343-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="83343-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="83343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83343-102">SYNOPSIS</span></span>
<span data-ttu-id="83343-103">Azure Event Grid에서 지원하는 토픽 유형에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83343-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="83343-104">구문</span><span class="sxs-lookup"><span data-stu-id="83343-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83343-105">설명</span><span class="sxs-lookup"><span data-stu-id="83343-105">DESCRIPTION</span></span>
<span data-ttu-id="83343-106">Azure Event Grid에서 지원하는 토픽 형식의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83343-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="83343-107">토픽 유형 이름을 지정하면 해당 토픽 유형에 대한 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="83343-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="83343-108">토픽 형식 이름을 지정하지 않으면 모든 토픽 유형에 대한 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="83343-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="83343-109">IncludeEventTypes를 지정하면 각 토픽 유형에서 지원하는 이벤트 유형에 대한 정보가 응답에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="83343-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="83343-110">예제</span><span class="sxs-lookup"><span data-stu-id="83343-110">EXAMPLES</span></span>

### <span data-ttu-id="83343-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="83343-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="83343-112">토픽 형식의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83343-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="83343-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="83343-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="83343-114">StorageAccounts 토픽 형식에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83343-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="83343-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="83343-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="83343-116">StorageAccounts에서 지원하는 이벤트 유형을 포함하여 StorageAccounts 토픽 형식에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83343-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="83343-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83343-117">PARAMETERS</span></span>

### <span data-ttu-id="83343-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83343-118">-DefaultProfile</span></span>
<span data-ttu-id="83343-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="83343-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83343-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="83343-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="83343-121">지정된 경우 응답에는 토픽 유형에서 지원하는 이벤트 형식이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="83343-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83343-122">-Name</span><span class="sxs-lookup"><span data-stu-id="83343-122">-Name</span></span>
<span data-ttu-id="83343-123">EventGrid 토픽 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83343-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83343-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83343-124">CommonParameters</span></span>
<span data-ttu-id="83343-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83343-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83343-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83343-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83343-127">입력</span><span class="sxs-lookup"><span data-stu-id="83343-127">INPUTS</span></span>

### <span data-ttu-id="83343-128">System.String</span><span class="sxs-lookup"><span data-stu-id="83343-128">System.String</span></span>

## <span data-ttu-id="83343-129">출력</span><span class="sxs-lookup"><span data-stu-id="83343-129">OUTPUTS</span></span>

### <span data-ttu-id="83343-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="83343-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="83343-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="83343-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="83343-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83343-132">NOTES</span></span>

## <span data-ttu-id="83343-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83343-133">RELATED LINKS</span></span>
