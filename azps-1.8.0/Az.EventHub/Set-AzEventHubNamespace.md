---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700809"
---
# <span data-ttu-id="f0b36-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f0b36-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="f0b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b36-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b36-103">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f0b36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0b36-104">SYNTAX</span></span>

### <span data-ttu-id="f0b36-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0b36-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b36-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b36-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b36-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f0b36-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b36-108">Set-AzEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f0b36-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f0b36-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b36-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0b36-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="f0b36-111">네임 스페이스 MyNamespaceName의 상태 \` \` 를 생성으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="f0b36-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f0b36-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="f0b36-113">\` \` Autoinflate = Enabled 및 MaximumThroughputUnits = 10 인 네임 스페이스 MyNamespaceName의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="f0b36-114">변수</span><span class="sxs-lookup"><span data-stu-id="f0b36-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b36-115">-DefaultProfile</span></span>
<span data-ttu-id="f0b36-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b36-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="f0b36-117">-EnableAutoInflate</span></span>
<span data-ttu-id="f0b36-118">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="f0b36-119">-위치</span><span class="sxs-lookup"><span data-stu-id="f0b36-119">-Location</span></span>
<span data-ttu-id="f0b36-120">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="f0b36-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="f0b36-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="f0b36-122">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b36-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f0b36-123">-Name</span></span>
<span data-ttu-id="f0b36-124">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="f0b36-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b36-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0b36-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0b36-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f0b36-127">-SkuCapacity</span></span>
<span data-ttu-id="f0b36-128">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="f0b36-129">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="f0b36-129">-SkuName</span></span>
<span data-ttu-id="f0b36-130">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="f0b36-131">-상태</span><span class="sxs-lookup"><span data-stu-id="f0b36-131">-State</span></span>
<span data-ttu-id="f0b36-132">네임 스페이스를 사용 하거나 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b36-133">태그</span><span class="sxs-lookup"><span data-stu-id="f0b36-133">-Tag</span></span>
<span data-ttu-id="f0b36-134">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b36-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f0b36-135">-Confirm</span></span>
<span data-ttu-id="f0b36-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b36-137">-WhatIf</span></span>
<span data-ttu-id="f0b36-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b36-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b36-140">CommonParameters</span></span>
<span data-ttu-id="f0b36-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b36-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b36-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b36-143">입력</span><span class="sxs-lookup"><span data-stu-id="f0b36-143">INPUTS</span></span>

### <span data-ttu-id="f0b36-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0b36-144">System.String</span></span>

### <span data-ttu-id="f0b36-145">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="f0b36-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0b36-146">시스템 Null 허용 ' 1 [[NamespaceState, [Microsoft Azure.]. h t m l. i = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f0b36-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f0b36-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f0b36-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0b36-148">출력</span><span class="sxs-lookup"><span data-stu-id="f0b36-148">OUTPUTS</span></span>

### <span data-ttu-id="f0b36-149">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="f0b36-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f0b36-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f0b36-150">NOTES</span></span>

## <span data-ttu-id="f0b36-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0b36-151">RELATED LINKS</span></span>
