---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212787"
---
# <span data-ttu-id="3a9de-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3a9de-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="3a9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9de-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9de-103">Azure 이벤트 그리드 도메인에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3a9de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a9de-104">SYNTAX</span></span>

### <span data-ttu-id="3a9de-105">DomainNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a9de-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9de-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a9de-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9de-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a9de-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9de-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3a9de-108">DESCRIPTION</span></span>
<span data-ttu-id="3a9de-109">Azure 이벤트 그리드 도메인에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3a9de-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3a9de-110">EXAMPLES</span></span>

### <span data-ttu-id="3a9de-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a9de-111">Example 1</span></span>

<span data-ttu-id="3a9de-112">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1 키 key1 ' \에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="3a9de-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3a9de-113">Example 2</span></span>

<span data-ttu-id="3a9de-114">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1 키 key1 ' \에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="3a9de-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="3a9de-115">Example 3</span></span>

<span data-ttu-id="3a9de-116">\' \` \` \` \` 전체 리소스 Id를 사용 하 여 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1의 키 key2 ' \ '에 해당 하는 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="3a9de-117">변수</span><span class="sxs-lookup"><span data-stu-id="3a9de-117">PARAMETERS</span></span>

### <span data-ttu-id="3a9de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9de-118">-DefaultProfile</span></span>
<span data-ttu-id="3a9de-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a9de-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="3a9de-120">-DomainInputObject</span></span>
<span data-ttu-id="3a9de-121">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="3a9de-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="3a9de-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="3a9de-122">-DomainName</span></span>
<span data-ttu-id="3a9de-123">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="3a9de-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="3a9de-124">-DomainResourceId</span></span>
<span data-ttu-id="3a9de-125">이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="3a9de-126">-이름</span><span class="sxs-lookup"><span data-stu-id="3a9de-126">-Name</span></span>
<span data-ttu-id="3a9de-127">다시 생성 해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="3a9de-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9de-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a9de-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a9de-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3a9de-130">-Confirm</span></span>
<span data-ttu-id="3a9de-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9de-132">-WhatIf</span></span>
<span data-ttu-id="3a9de-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9de-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9de-135">CommonParameters</span></span>
<span data-ttu-id="3a9de-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9de-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a9de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9de-138">입력</span><span class="sxs-lookup"><span data-stu-id="3a9de-138">INPUTS</span></span>

### <span data-ttu-id="3a9de-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a9de-139">System.String</span></span>

### <span data-ttu-id="3a9de-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="3a9de-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="3a9de-141">출력</span><span class="sxs-lookup"><span data-stu-id="3a9de-141">OUTPUTS</span></span>

### <span data-ttu-id="3a9de-142">Microsoft. Azure. 관리. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3a9de-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="3a9de-143">상속자</span><span class="sxs-lookup"><span data-stu-id="3a9de-143">NOTES</span></span>

## <span data-ttu-id="3a9de-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a9de-144">RELATED LINKS</span></span>
