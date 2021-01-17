---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329517"
---
# <span data-ttu-id="994dc-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="994dc-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="994dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994dc-102">SYNOPSIS</span></span>
<span data-ttu-id="994dc-103">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="994dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="994dc-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="994dc-105">설명</span><span class="sxs-lookup"><span data-stu-id="994dc-105">DESCRIPTION</span></span>
<span data-ttu-id="994dc-106">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="994dc-107">예제</span><span class="sxs-lookup"><span data-stu-id="994dc-107">EXAMPLES</span></span>

### <span data-ttu-id="994dc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="994dc-108">Example 1</span></span>

<span data-ttu-id="994dc-109">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Domain Domain1에서 Event Grid 도메인 토픽 토픽1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="994dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="994dc-110">PARAMETERS</span></span>

### <span data-ttu-id="994dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994dc-111">-DefaultProfile</span></span>
<span data-ttu-id="994dc-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="994dc-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="994dc-113">-DomainName</span></span>
<span data-ttu-id="994dc-114">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="994dc-115">-Name</span></span>
<span data-ttu-id="994dc-116">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="994dc-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994dc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="994dc-119">-Confirm</span></span>
<span data-ttu-id="994dc-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994dc-121">-WhatIf</span></span>
<span data-ttu-id="994dc-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="994dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994dc-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994dc-124">CommonParameters</span></span>
<span data-ttu-id="994dc-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="994dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994dc-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="994dc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994dc-127">입력</span><span class="sxs-lookup"><span data-stu-id="994dc-127">INPUTS</span></span>

### <span data-ttu-id="994dc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="994dc-128">System.String</span></span>

## <span data-ttu-id="994dc-129">출력</span><span class="sxs-lookup"><span data-stu-id="994dc-129">OUTPUTS</span></span>

### <span data-ttu-id="994dc-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="994dc-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="994dc-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="994dc-131">NOTES</span></span>

## <span data-ttu-id="994dc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="994dc-132">RELATED LINKS</span></span>
