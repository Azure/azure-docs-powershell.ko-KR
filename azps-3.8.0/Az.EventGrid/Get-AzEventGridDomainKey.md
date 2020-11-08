---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: f4bc6e7b505f48fe335a5bbc19703032e9ecf06d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034173"
---
# <span data-ttu-id="f5281-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f5281-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="f5281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5281-102">SYNOPSIS</span></span>
<span data-ttu-id="f5281-103">이벤트를 이벤트 그리드 도메인에 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="f5281-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5281-104">SYNTAX</span></span>

### <span data-ttu-id="f5281-105">DomainNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5281-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5281-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5281-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5281-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5281-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5281-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f5281-108">DESCRIPTION</span></span>
<span data-ttu-id="f5281-109">이벤트를 이벤트 그리드 도메인에 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="f5281-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f5281-110">EXAMPLES</span></span>

### <span data-ttu-id="f5281-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5281-111">Example 1</span></span>

<span data-ttu-id="f5281-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 공유 된 선택 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f5281-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="f5281-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5281-113">Example 2</span></span>

<span data-ttu-id="f5281-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 공유 된 선택 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f5281-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="f5281-115">변수</span><span class="sxs-lookup"><span data-stu-id="f5281-115">PARAMETERS</span></span>

### <span data-ttu-id="f5281-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5281-116">-DefaultProfile</span></span>
<span data-ttu-id="f5281-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5281-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="f5281-118">-DomainObject</span></span>
<span data-ttu-id="f5281-119">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="f5281-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5281-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="f5281-120">-DomainResourceId</span></span>
<span data-ttu-id="f5281-121">이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-121">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5281-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f5281-122">-Name</span></span>
<span data-ttu-id="f5281-123">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5281-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5281-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5281-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5281-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5281-126">CommonParameters</span></span>
<span data-ttu-id="f5281-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5281-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5281-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5281-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5281-129">입력</span><span class="sxs-lookup"><span data-stu-id="f5281-129">INPUTS</span></span>

### <span data-ttu-id="f5281-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5281-130">System.String</span></span>

### <span data-ttu-id="f5281-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="f5281-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="f5281-132">출력</span><span class="sxs-lookup"><span data-stu-id="f5281-132">OUTPUTS</span></span>

### <span data-ttu-id="f5281-133">Microsoft. Azure. 관리. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f5281-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="f5281-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f5281-134">NOTES</span></span>

## <span data-ttu-id="f5281-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5281-135">RELATED LINKS</span></span>
