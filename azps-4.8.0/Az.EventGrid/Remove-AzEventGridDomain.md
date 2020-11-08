---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214991"
---
# <span data-ttu-id="0a99e-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a99e-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="0a99e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a99e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a99e-103">Azure 이벤트 그리드 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="0a99e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a99e-104">SYNTAX</span></span>

### <span data-ttu-id="0a99e-105">DomainNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a99e-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a99e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a99e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a99e-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a99e-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a99e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0a99e-108">DESCRIPTION</span></span>
<span data-ttu-id="0a99e-109">Azure 이벤트 그리드 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="0a99e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0a99e-110">EXAMPLES</span></span>

### <span data-ttu-id="0a99e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a99e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="0a99e-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="0a99e-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0a99e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0a99e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="0a99e-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="0a99e-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0a99e-115">변수</span><span class="sxs-lookup"><span data-stu-id="0a99e-115">PARAMETERS</span></span>

### <span data-ttu-id="0a99e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a99e-116">-DefaultProfile</span></span>
<span data-ttu-id="0a99e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a99e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a99e-118">-InputObject</span></span>
<span data-ttu-id="0a99e-119">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="0a99e-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="0a99e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0a99e-120">-Name</span></span>
<span data-ttu-id="0a99e-121">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="0a99e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a99e-122">-PassThru</span></span>
<span data-ttu-id="0a99e-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="0a99e-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0a99e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a99e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a99e-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a99e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a99e-126">-ResourceId</span></span>
<span data-ttu-id="0a99e-127">이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a99e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0a99e-128">-Confirm</span></span>
<span data-ttu-id="0a99e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a99e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a99e-130">-WhatIf</span></span>
<span data-ttu-id="0a99e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a99e-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a99e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a99e-133">CommonParameters</span></span>
<span data-ttu-id="0a99e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a99e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a99e-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a99e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a99e-136">입력</span><span class="sxs-lookup"><span data-stu-id="0a99e-136">INPUTS</span></span>

### <span data-ttu-id="0a99e-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0a99e-137">System.String</span></span>

### <span data-ttu-id="0a99e-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="0a99e-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="0a99e-139">출력</span><span class="sxs-lookup"><span data-stu-id="0a99e-139">OUTPUTS</span></span>

### <span data-ttu-id="0a99e-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0a99e-140">System.Boolean</span></span>

## <span data-ttu-id="0a99e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0a99e-141">NOTES</span></span>

## <span data-ttu-id="0a99e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a99e-142">RELATED LINKS</span></span>
