---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: cd3182a2a00f488dabd70a97d06693362068768c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535171"
---
# <span data-ttu-id="88a55-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="88a55-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="88a55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a55-102">SYNOPSIS</span></span>
<span data-ttu-id="88a55-103">Azure 이벤트 표에서 지원 되는 항목 형식에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88a55-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88a55-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88a55-105">DESCRIPTION</span></span>
<span data-ttu-id="88a55-106">Azure 이벤트 표에서 지원 되는 항목 종류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="88a55-107">주제 형식 이름을 지정 하면 해당 주제 형식에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="88a55-108">주제 형식 이름을 지정 하지 않으면 모든 항목 종류에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="88a55-109">IncludeEventTypes가 지정 된 경우 각 항목 유형에 의해 지원 되는 이벤트 유형에 대 한 정보가 응답에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="88a55-110">예제의</span><span class="sxs-lookup"><span data-stu-id="88a55-110">EXAMPLES</span></span>

### <span data-ttu-id="88a55-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="88a55-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="88a55-112">항목 형식의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="88a55-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="88a55-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="88a55-114">StorageAccounts 항목 형식에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="88a55-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="88a55-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="88a55-116">StorageAccounts에서 지원 되는 이벤트 유형을 비롯 하 여 StorageAccounts 주제 유형에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="88a55-117">변수</span><span class="sxs-lookup"><span data-stu-id="88a55-117">PARAMETERS</span></span>

### <span data-ttu-id="88a55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a55-118">-DefaultProfile</span></span>
<span data-ttu-id="88a55-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88a55-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88a55-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="88a55-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="88a55-121">지정 되는 경우 응답에는 항목 형식에서 지원 되는 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="88a55-122">-이름</span><span class="sxs-lookup"><span data-stu-id="88a55-122">-Name</span></span>
<span data-ttu-id="88a55-123">EventGrid 주제 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="88a55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a55-124">CommonParameters</span></span>
<span data-ttu-id="88a55-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88a55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a55-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a55-127">입력</span><span class="sxs-lookup"><span data-stu-id="88a55-127">INPUTS</span></span>

### <span data-ttu-id="88a55-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88a55-128">System.String</span></span>

## <span data-ttu-id="88a55-129">출력</span><span class="sxs-lookup"><span data-stu-id="88a55-129">OUTPUTS</span></span>

### <span data-ttu-id="88a55-130">Microsoft. PSTopicTypeInfoListInstance 표.</span><span class="sxs-lookup"><span data-stu-id="88a55-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="88a55-131">Microsoft. Azure.. m a m. 모델.</span><span class="sxs-lookup"><span data-stu-id="88a55-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="88a55-132">상속자</span><span class="sxs-lookup"><span data-stu-id="88a55-132">NOTES</span></span>

## <span data-ttu-id="88a55-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88a55-133">RELATED LINKS</span></span>