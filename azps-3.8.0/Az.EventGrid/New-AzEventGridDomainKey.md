---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: fe86115ec5b82570a8498db10efeb7b7b24dd9c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878297"
---
# <span data-ttu-id="05b08-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="05b08-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="05b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b08-102">SYNOPSIS</span></span>
<span data-ttu-id="05b08-103">Azure 이벤트 그리드 도메인에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="05b08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05b08-104">SYNTAX</span></span>

### <span data-ttu-id="05b08-105">DomainNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="05b08-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b08-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b08-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b08-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b08-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b08-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05b08-108">DESCRIPTION</span></span>
<span data-ttu-id="05b08-109">Azure 이벤트 그리드 도메인에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="05b08-110">예제의</span><span class="sxs-lookup"><span data-stu-id="05b08-110">EXAMPLES</span></span>

### <span data-ttu-id="05b08-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="05b08-111">Example 1</span></span>

<span data-ttu-id="05b08-112">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1 키 key1 ' \에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="05b08-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="05b08-113">Example 2</span></span>

<span data-ttu-id="05b08-114">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1 키 key1 ' \에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="05b08-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="05b08-115">Example 3</span></span>

<span data-ttu-id="05b08-116">\' \` \` \` \` 전체 리소스 Id를 사용 하 여 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1의 키 key2 ' \ '에 해당 하는 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="05b08-117">변수</span><span class="sxs-lookup"><span data-stu-id="05b08-117">PARAMETERS</span></span>

### <span data-ttu-id="05b08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b08-118">-DefaultProfile</span></span>
<span data-ttu-id="05b08-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05b08-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="05b08-120">-DomainInputObject</span></span>
<span data-ttu-id="05b08-121">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="05b08-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="05b08-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="05b08-122">-DomainName</span></span>
<span data-ttu-id="05b08-123">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b08-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="05b08-124">-DomainResourceId</span></span>
<span data-ttu-id="05b08-125">이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="05b08-126">-이름</span><span class="sxs-lookup"><span data-stu-id="05b08-126">-Name</span></span>
<span data-ttu-id="05b08-127">다시 생성 해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b08-128">-ResourceGroupName</span></span>
<span data-ttu-id="05b08-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="05b08-130">-확인</span><span class="sxs-lookup"><span data-stu-id="05b08-130">-Confirm</span></span>
<span data-ttu-id="05b08-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b08-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b08-132">-WhatIf</span></span>
<span data-ttu-id="05b08-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b08-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b08-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b08-135">CommonParameters</span></span>
<span data-ttu-id="05b08-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b08-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b08-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b08-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b08-138">입력</span><span class="sxs-lookup"><span data-stu-id="05b08-138">INPUTS</span></span>

### <span data-ttu-id="05b08-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05b08-139">System.String</span></span>

### <span data-ttu-id="05b08-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="05b08-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="05b08-141">출력</span><span class="sxs-lookup"><span data-stu-id="05b08-141">OUTPUTS</span></span>

### <span data-ttu-id="05b08-142">Microsoft. Azure. 관리. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="05b08-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="05b08-143">상속자</span><span class="sxs-lookup"><span data-stu-id="05b08-143">NOTES</span></span>

## <span data-ttu-id="05b08-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05b08-144">RELATED LINKS</span></span>
