---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527583"
---
# <span data-ttu-id="7c051-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7c051-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="7c051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c051-102">SYNOPSIS</span></span>
<span data-ttu-id="7c051-103">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c051-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c051-104">SYNTAX</span></span>

### <span data-ttu-id="7c051-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c051-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7c051-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c051-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7c051-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c051-107">DESCRIPTION</span></span>
<span data-ttu-id="7c051-108">Set-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7c051-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c051-109">EXAMPLES</span></span>

### <span data-ttu-id="7c051-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c051-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="7c051-111">네임 스페이스 MyNamespaceName의 상태 \` \` 를 생성으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="7c051-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c051-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="7c051-113">\` \` Autoinflate = Enabled 및 MaximumThroughputUnits = 10 인 네임 스페이스 MyNamespaceName의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="7c051-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c051-114">PARAMETERS</span></span>

### <span data-ttu-id="7c051-115">-위치</span><span class="sxs-lookup"><span data-stu-id="7c051-115">-Location</span></span>
<span data-ttu-id="7c051-116">이벤트 허브 네임 스페이스 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="7c051-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c051-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c051-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-118">Resource group name.</span></span>

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

### <span data-ttu-id="7c051-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7c051-119">-SkuCapacity</span></span>
<span data-ttu-id="7c051-120">이벤트 허브 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="7c051-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="7c051-121">-SkuName</span></span>
<span data-ttu-id="7c051-122">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c051-123">-상태</span><span class="sxs-lookup"><span data-stu-id="7c051-123">-State</span></span>
<span data-ttu-id="7c051-124">네임 스페이스의 상태 (사용 안 함 또는 사용 가능)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c051-125">태그</span><span class="sxs-lookup"><span data-stu-id="7c051-125">-Tag</span></span>
<span data-ttu-id="7c051-126">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="7c051-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="7c051-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7c051-127">-Confirm</span></span>
<span data-ttu-id="7c051-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c051-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c051-129">-WhatIf</span></span>
<span data-ttu-id="7c051-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c051-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c051-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7c051-132">-EnableAutoInflate</span></span>
<span data-ttu-id="7c051-133">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="7c051-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7c051-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7c051-135">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값이 0 ~ 20 개 범위 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="7c051-136">-이름</span><span class="sxs-lookup"><span data-stu-id="7c051-136">-Name</span></span>
<span data-ttu-id="7c051-137">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="7c051-138">입력</span><span class="sxs-lookup"><span data-stu-id="7c051-138">INPUTS</span></span>

### <span data-ttu-id="7c051-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c051-139">System.String</span></span>

### <span data-ttu-id="7c051-140">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7c051-140">System.Int32</span></span>

### <span data-ttu-id="7c051-141">NamespaceState를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c051-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="7c051-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7c051-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c051-143">출력</span><span class="sxs-lookup"><span data-stu-id="7c051-143">OUTPUTS</span></span>

### <span data-ttu-id="7c051-144">NamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="7c051-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="7c051-145">상속자</span><span class="sxs-lookup"><span data-stu-id="7c051-145">NOTES</span></span>

## <span data-ttu-id="7c051-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c051-146">RELATED LINKS</span></span>

