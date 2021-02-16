---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209600"
---
# <span data-ttu-id="b19c2-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b19c2-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="b19c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b19c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b19c2-103">Event Grid 도메인에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="b19c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="b19c2-104">SYNTAX</span></span>

### <span data-ttu-id="b19c2-105">DomainNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b19c2-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b19c2-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b19c2-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b19c2-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b19c2-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b19c2-108">설명</span><span class="sxs-lookup"><span data-stu-id="b19c2-108">DESCRIPTION</span></span>
<span data-ttu-id="b19c2-109">Event Grid 도메인에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="b19c2-110">예제</span><span class="sxs-lookup"><span data-stu-id="b19c2-110">EXAMPLES</span></span>

### <span data-ttu-id="b19c2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b19c2-111">Example 1</span></span>

<span data-ttu-id="b19c2-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 Domain1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="b19c2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b19c2-113">Example 2</span></span>

<span data-ttu-id="b19c2-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 Domain1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="b19c2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b19c2-115">PARAMETERS</span></span>

### <span data-ttu-id="b19c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19c2-116">-DefaultProfile</span></span>
<span data-ttu-id="b19c2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b19c2-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="b19c2-118">-DomainObject</span></span>
<span data-ttu-id="b19c2-119">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="b19c2-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="b19c2-120">-DomainResourceId</span></span>
<span data-ttu-id="b19c2-121">Event Grid 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="b19c2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b19c2-122">-Name</span></span>
<span data-ttu-id="b19c2-123">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b19c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b19c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b19c2-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b19c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19c2-126">CommonParameters</span></span>
<span data-ttu-id="b19c2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b19c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19c2-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b19c2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19c2-129">입력</span><span class="sxs-lookup"><span data-stu-id="b19c2-129">INPUTS</span></span>

### <span data-ttu-id="b19c2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b19c2-130">System.String</span></span>

### <span data-ttu-id="b19c2-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="b19c2-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="b19c2-132">출력</span><span class="sxs-lookup"><span data-stu-id="b19c2-132">OUTPUTS</span></span>

### <span data-ttu-id="b19c2-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b19c2-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="b19c2-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b19c2-134">NOTES</span></span>

## <span data-ttu-id="b19c2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b19c2-135">RELATED LINKS</span></span>
