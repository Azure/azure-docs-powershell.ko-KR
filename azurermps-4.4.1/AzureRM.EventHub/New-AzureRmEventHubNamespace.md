---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711572"
---
# <span data-ttu-id="6c56d-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6c56d-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="6c56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c56d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c56d-103">이벤트 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c56d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c56d-104">SYNTAX</span></span>

### <span data-ttu-id="6c56d-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c56d-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6c56d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c56d-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6c56d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6c56d-107">DESCRIPTION</span></span>
<span data-ttu-id="6c56d-108">New-AzureRmEventHubNamespace cmdlet은 이벤트 허브 유형의 새 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="6c56d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6c56d-109">EXAMPLES</span></span>

### <span data-ttu-id="6c56d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c56d-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="6c56d-111">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Mylocation에 이벤트 \` 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="6c56d-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6c56d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6c56d-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="6c56d-113">\`지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만들고 \` \` \` , 리소스 그룹 \` MyResourceGroupName에서 \` MaximumThroughputUnits 10으로 autoinflate을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="6c56d-114">변수</span><span class="sxs-lookup"><span data-stu-id="6c56d-114">PARAMETERS</span></span>

### <span data-ttu-id="6c56d-115">-위치</span><span class="sxs-lookup"><span data-stu-id="6c56d-115">-Location</span></span>
<span data-ttu-id="6c56d-116">이벤트 허브 네임 스페이스 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c56d-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c56d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6c56d-119">-SkuCapacity</span></span>
<span data-ttu-id="6c56d-120">이벤트 허브 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="6c56d-121">-SkuName</span></span>
<span data-ttu-id="6c56d-122">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-123">태그</span><span class="sxs-lookup"><span data-stu-id="6c56d-123">-Tag</span></span>
<span data-ttu-id="6c56d-124">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="6c56d-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="6c56d-125">-Confirm</span></span>
<span data-ttu-id="6c56d-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c56d-127">-WhatIf</span></span>
<span data-ttu-id="6c56d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c56d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="6c56d-130">-EnableAutoInflate</span></span>
<span data-ttu-id="6c56d-131">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="6c56d-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="6c56d-133">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값이 0 ~ 20 개 범위 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c56d-134">-이름</span><span class="sxs-lookup"><span data-stu-id="6c56d-134">-Name</span></span>
<span data-ttu-id="6c56d-135">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c56d-135">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6c56d-136">입력</span><span class="sxs-lookup"><span data-stu-id="6c56d-136">INPUTS</span></span>

### <span data-ttu-id="6c56d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6c56d-137">System.String</span></span>
<span data-ttu-id="6c56d-138">시스템. \` \[ \[ Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, publickeytoken = B77a5c561934e089 \] \] system. Null 허용 \` 1 \[ \[ 시스템. 부울, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089 \] \] system.webserver</span><span class="sxs-lookup"><span data-stu-id="6c56d-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c56d-139">출력</span><span class="sxs-lookup"><span data-stu-id="6c56d-139">OUTPUTS</span></span>

### <span data-ttu-id="6c56d-140">NamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="6c56d-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="6c56d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6c56d-141">NOTES</span></span>

## <span data-ttu-id="6c56d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c56d-142">RELATED LINKS</span></span>

