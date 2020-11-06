---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 739d027d095810ae33f90a7b5cc1ad7caf148081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529837"
---
# <span data-ttu-id="9fa1d-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9fa1d-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="9fa1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa1d-103">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fa1d-104">SYNTAX</span></span>

### <span data-ttu-id="9fa1d-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9fa1d-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa1d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fa1d-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa1d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9fa1d-107">DESCRIPTION</span></span>
<span data-ttu-id="9fa1d-108">Set-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9fa1d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9fa1d-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa1d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fa1d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="9fa1d-111">네임 스페이스 MyNamespaceName의 상태 \` \` 를 생성으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="9fa1d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9fa1d-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="9fa1d-113">\` \` Autoinflate = Enabled 및 MaximumThroughputUnits = 10 인 네임 스페이스 MyNamespaceName의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="9fa1d-114">변수</span><span class="sxs-lookup"><span data-stu-id="9fa1d-114">PARAMETERS</span></span>

### <span data-ttu-id="9fa1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa1d-115">-DefaultProfile</span></span>
<span data-ttu-id="9fa1d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="9fa1d-117">-EnableAutoInflate</span></span>
<span data-ttu-id="9fa1d-118">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-119">-위치</span><span class="sxs-lookup"><span data-stu-id="9fa1d-119">-Location</span></span>
<span data-ttu-id="9fa1d-120">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="9fa1d-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="9fa1d-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="9fa1d-122">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9fa1d-123">-Name</span></span>
<span data-ttu-id="9fa1d-124">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="9fa1d-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="9fa1d-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9fa1d-127">-SkuCapacity</span></span>
<span data-ttu-id="9fa1d-128">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-129">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="9fa1d-129">-SkuName</span></span>
<span data-ttu-id="9fa1d-130">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="9fa1d-131">-상태</span><span class="sxs-lookup"><span data-stu-id="9fa1d-131">-State</span></span>
<span data-ttu-id="9fa1d-132">네임 스페이스를 사용 하거나 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-132">Disable/Enable Namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-133">태그</span><span class="sxs-lookup"><span data-stu-id="9fa1d-133">-Tag</span></span>
<span data-ttu-id="9fa1d-134">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9fa1d-135">-Confirm</span></span>
<span data-ttu-id="9fa1d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa1d-137">-WhatIf</span></span>
<span data-ttu-id="9fa1d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa1d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa1d-140">CommonParameters</span></span>
<span data-ttu-id="9fa1d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9fa1d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa1d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa1d-143">입력</span><span class="sxs-lookup"><span data-stu-id="9fa1d-143">INPUTS</span></span>

### <span data-ttu-id="9fa1d-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9fa1d-144">System.String</span></span>
<span data-ttu-id="9fa1d-145">시스템. Null 허용 `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[[NamespaceState, microsoft azure. 0.5.0.0,, Culture = 중립, PublicKeyToken = null]) system.webserver. 컬렉션</span><span class="sxs-lookup"><span data-stu-id="9fa1d-145">System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="9fa1d-146">출력</span><span class="sxs-lookup"><span data-stu-id="9fa1d-146">OUTPUTS</span></span>

### <span data-ttu-id="9fa1d-147">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="9fa1d-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="9fa1d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9fa1d-148">NOTES</span></span>

## <span data-ttu-id="9fa1d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fa1d-149">RELATED LINKS</span></span>
