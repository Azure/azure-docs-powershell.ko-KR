---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 18be852a8a44f55cbc159bdbc7b4dbf3f276582a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991279"
---
# <span data-ttu-id="94529-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="94529-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="94529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94529-102">SYNOPSIS</span></span>
<span data-ttu-id="94529-103">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94529-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="94529-104">구문</span><span class="sxs-lookup"><span data-stu-id="94529-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94529-105">설명</span><span class="sxs-lookup"><span data-stu-id="94529-105">DESCRIPTION</span></span>
<span data-ttu-id="94529-106">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94529-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="94529-107">예제</span><span class="sxs-lookup"><span data-stu-id="94529-107">EXAMPLES</span></span>

### <span data-ttu-id="94529-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="94529-108">Example 1</span></span>

<span data-ttu-id="94529-109">리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 Domain Domain1에서 Event Grid 도메인 토픽1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94529-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="94529-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94529-110">PARAMETERS</span></span>

### <span data-ttu-id="94529-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94529-111">-DefaultProfile</span></span>
<span data-ttu-id="94529-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94529-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94529-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="94529-113">-DomainName</span></span>
<span data-ttu-id="94529-114">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94529-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="94529-115">-Name</span><span class="sxs-lookup"><span data-stu-id="94529-115">-Name</span></span>
<span data-ttu-id="94529-116">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94529-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="94529-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94529-117">-ResourceGroupName</span></span>
<span data-ttu-id="94529-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94529-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="94529-119">-확인</span><span class="sxs-lookup"><span data-stu-id="94529-119">-Confirm</span></span>
<span data-ttu-id="94529-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94529-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94529-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94529-121">-WhatIf</span></span>
<span data-ttu-id="94529-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="94529-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94529-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94529-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94529-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94529-124">CommonParameters</span></span>
<span data-ttu-id="94529-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94529-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94529-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94529-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94529-127">입력</span><span class="sxs-lookup"><span data-stu-id="94529-127">INPUTS</span></span>

### <span data-ttu-id="94529-128">System.String</span><span class="sxs-lookup"><span data-stu-id="94529-128">System.String</span></span>

## <span data-ttu-id="94529-129">출력</span><span class="sxs-lookup"><span data-stu-id="94529-129">OUTPUTS</span></span>

### <span data-ttu-id="94529-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="94529-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="94529-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94529-131">NOTES</span></span>

## <span data-ttu-id="94529-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94529-132">RELATED LINKS</span></span>
