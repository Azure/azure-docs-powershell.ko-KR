---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214538"
---
# <span data-ttu-id="ec578-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ec578-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ec578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec578-102">SYNOPSIS</span></span>
<span data-ttu-id="ec578-103">새 Azure 이벤트 그리드 도메인 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ec578-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec578-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec578-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec578-105">DESCRIPTION</span></span>
<span data-ttu-id="ec578-106">새 Azure 이벤트 그리드 도메인 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ec578-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec578-107">EXAMPLES</span></span>

### <span data-ttu-id="ec578-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec578-108">Example 1</span></span>

<span data-ttu-id="ec578-109">\` \` \` \` 리소스 그룹 MyResourceGroupName의 도메인 Domain1에 Topic1 \` 이벤트 그리드 도메인 항목을 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="ec578-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="ec578-110">변수</span><span class="sxs-lookup"><span data-stu-id="ec578-110">PARAMETERS</span></span>

### <span data-ttu-id="ec578-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec578-111">-DefaultProfile</span></span>
<span data-ttu-id="ec578-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec578-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ec578-113">-DomainName</span></span>
<span data-ttu-id="ec578-114">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ec578-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ec578-115">-Name</span></span>
<span data-ttu-id="ec578-116">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ec578-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec578-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec578-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec578-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ec578-119">-Confirm</span></span>
<span data-ttu-id="ec578-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec578-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec578-121">-WhatIf</span></span>
<span data-ttu-id="ec578-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec578-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec578-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec578-124">CommonParameters</span></span>
<span data-ttu-id="ec578-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec578-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec578-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec578-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec578-127">입력</span><span class="sxs-lookup"><span data-stu-id="ec578-127">INPUTS</span></span>

### <span data-ttu-id="ec578-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec578-128">System.String</span></span>

## <span data-ttu-id="ec578-129">출력</span><span class="sxs-lookup"><span data-stu-id="ec578-129">OUTPUTS</span></span>

### <span data-ttu-id="ec578-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ec578-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="ec578-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ec578-131">NOTES</span></span>

## <span data-ttu-id="ec578-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec578-132">RELATED LINKS</span></span>
