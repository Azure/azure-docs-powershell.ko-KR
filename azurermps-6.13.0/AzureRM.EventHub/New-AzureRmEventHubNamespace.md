---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702940"
---
# <span data-ttu-id="80658-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="80658-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="80658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80658-102">SYNOPSIS</span></span>
<span data-ttu-id="80658-103">이벤트 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80658-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80658-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80658-104">SYNTAX</span></span>

### <span data-ttu-id="80658-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="80658-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80658-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="80658-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80658-107">설명은</span><span class="sxs-lookup"><span data-stu-id="80658-107">DESCRIPTION</span></span>
<span data-ttu-id="80658-108">New-AzureRmEventHubNamespace cmdlet은 이벤트 허브 유형의 새 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80658-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="80658-109">예제의</span><span class="sxs-lookup"><span data-stu-id="80658-109">EXAMPLES</span></span>

### <span data-ttu-id="80658-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="80658-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="80658-111">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Mylocation에 이벤트 \` 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="80658-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="80658-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="80658-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="80658-113">\`지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만들고 \` \` \` , 리소스 그룹 \` MyResourceGroupName에서 \` MaximumThroughputUnits 10으로 autoinflate을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80658-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="80658-114">예제 3-Kafka 사용 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="80658-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="80658-115">\` \` \` \` \` Kafka 및 autoinflate을 사용 하는 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="80658-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="80658-116">변수</span><span class="sxs-lookup"><span data-stu-id="80658-116">PARAMETERS</span></span>

### <span data-ttu-id="80658-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80658-117">-DefaultProfile</span></span>
<span data-ttu-id="80658-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80658-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80658-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="80658-119">-EnableAutoInflate</span></span>
<span data-ttu-id="80658-120">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80658-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80658-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="80658-121">-EnableKafka</span></span>
<span data-ttu-id="80658-122">네임 스페이스의 Kafka을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="80658-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="80658-123">-위치</span><span class="sxs-lookup"><span data-stu-id="80658-123">-Location</span></span>
<span data-ttu-id="80658-124">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="80658-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="80658-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="80658-126">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80658-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-127">-이름</span><span class="sxs-lookup"><span data-stu-id="80658-127">-Name</span></span>
<span data-ttu-id="80658-128">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80658-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80658-129">-ResourceGroupName</span></span>
<span data-ttu-id="80658-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="80658-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="80658-131">-SkuCapacity</span></span>
<span data-ttu-id="80658-132">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="80658-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-133">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="80658-133">-SkuName</span></span>
<span data-ttu-id="80658-134">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80658-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-135">태그</span><span class="sxs-lookup"><span data-stu-id="80658-135">-Tag</span></span>
<span data-ttu-id="80658-136">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="80658-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80658-137">-확인</span><span class="sxs-lookup"><span data-stu-id="80658-137">-Confirm</span></span>
<span data-ttu-id="80658-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80658-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80658-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80658-139">-WhatIf</span></span>
<span data-ttu-id="80658-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80658-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80658-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80658-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80658-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80658-142">CommonParameters</span></span>
<span data-ttu-id="80658-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80658-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80658-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80658-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80658-145">입력</span><span class="sxs-lookup"><span data-stu-id="80658-145">INPUTS</span></span>


## <span data-ttu-id="80658-146">출력</span><span class="sxs-lookup"><span data-stu-id="80658-146">OUTPUTS</span></span>

### <span data-ttu-id="80658-147">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="80658-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="80658-148">상속자</span><span class="sxs-lookup"><span data-stu-id="80658-148">NOTES</span></span>

## <span data-ttu-id="80658-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80658-149">RELATED LINKS</span></span>
