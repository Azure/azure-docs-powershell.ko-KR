---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346761"
---
# <span data-ttu-id="2126a-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2126a-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="2126a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2126a-102">SYNOPSIS</span></span>
<span data-ttu-id="2126a-103">Event Grid 도메인에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="2126a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2126a-104">SYNTAX</span></span>

### <span data-ttu-id="2126a-105">DomainNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2126a-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2126a-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2126a-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2126a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2126a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2126a-108">설명</span><span class="sxs-lookup"><span data-stu-id="2126a-108">DESCRIPTION</span></span>
<span data-ttu-id="2126a-109">Event Grid 도메인에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="2126a-110">예제</span><span class="sxs-lookup"><span data-stu-id="2126a-110">EXAMPLES</span></span>

### <span data-ttu-id="2126a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2126a-111">Example 1</span></span>

<span data-ttu-id="2126a-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 Domain1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="2126a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2126a-113">Example 2</span></span>

<span data-ttu-id="2126a-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 Domain1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="2126a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2126a-115">PARAMETERS</span></span>

### <span data-ttu-id="2126a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2126a-116">-DefaultProfile</span></span>
<span data-ttu-id="2126a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2126a-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="2126a-118">-DomainObject</span></span>
<span data-ttu-id="2126a-119">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="2126a-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="2126a-120">-DomainResourceId</span></span>
<span data-ttu-id="2126a-121">Event Grid 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="2126a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2126a-122">-Name</span></span>
<span data-ttu-id="2126a-123">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2126a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2126a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2126a-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2126a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2126a-126">CommonParameters</span></span>
<span data-ttu-id="2126a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2126a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2126a-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2126a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2126a-129">입력</span><span class="sxs-lookup"><span data-stu-id="2126a-129">INPUTS</span></span>

### <span data-ttu-id="2126a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2126a-130">System.String</span></span>

### <span data-ttu-id="2126a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="2126a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="2126a-132">출력</span><span class="sxs-lookup"><span data-stu-id="2126a-132">OUTPUTS</span></span>

### <span data-ttu-id="2126a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2126a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="2126a-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2126a-134">NOTES</span></span>

## <span data-ttu-id="2126a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2126a-135">RELATED LINKS</span></span>
