---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: af46e09571deba338d67b75659f6915ac0e8e061
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875890"
---
# <span data-ttu-id="018aa-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="018aa-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="018aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018aa-102">SYNOPSIS</span></span>
<span data-ttu-id="018aa-103">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="018aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="018aa-104">SYNTAX</span></span>

### <span data-ttu-id="018aa-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="018aa-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="018aa-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="018aa-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018aa-107">설명은</span><span class="sxs-lookup"><span data-stu-id="018aa-107">DESCRIPTION</span></span>
<span data-ttu-id="018aa-108">Set-AzEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="018aa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="018aa-109">EXAMPLES</span></span>

### <span data-ttu-id="018aa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="018aa-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="018aa-111">네임 스페이스 MyNamespaceName의 태그 \` \` 를 생성으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="018aa-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="018aa-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="018aa-113">\` \` Autoinflate = Enabled 및 MaximumThroughputUnits = 10 인 네임 스페이스 MyNamespaceName의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="018aa-114">변수</span><span class="sxs-lookup"><span data-stu-id="018aa-114">PARAMETERS</span></span>

### <span data-ttu-id="018aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018aa-115">-DefaultProfile</span></span>
<span data-ttu-id="018aa-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018aa-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="018aa-117">-EnableAutoInflate</span></span>
<span data-ttu-id="018aa-118">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="018aa-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="018aa-119">-EnableKafka</span></span>
<span data-ttu-id="018aa-120">네임 스페이스의 Kafka을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="018aa-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="018aa-121">-위치</span><span class="sxs-lookup"><span data-stu-id="018aa-121">-Location</span></span>
<span data-ttu-id="018aa-122">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="018aa-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="018aa-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="018aa-124">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="018aa-125">-이름</span><span class="sxs-lookup"><span data-stu-id="018aa-125">-Name</span></span>
<span data-ttu-id="018aa-126">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="018aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="018aa-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="018aa-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="018aa-129">-SkuCapacity</span></span>
<span data-ttu-id="018aa-130">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="018aa-131">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="018aa-131">-SkuName</span></span>
<span data-ttu-id="018aa-132">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="018aa-133">-상태</span><span class="sxs-lookup"><span data-stu-id="018aa-133">-State</span></span>
<span data-ttu-id="018aa-134">네임 스페이스를 사용 하거나 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-134">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="018aa-135">태그</span><span class="sxs-lookup"><span data-stu-id="018aa-135">-Tag</span></span>
<span data-ttu-id="018aa-136">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="018aa-137">-확인</span><span class="sxs-lookup"><span data-stu-id="018aa-137">-Confirm</span></span>
<span data-ttu-id="018aa-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018aa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018aa-139">-WhatIf</span></span>
<span data-ttu-id="018aa-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="018aa-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018aa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018aa-142">CommonParameters</span></span>
<span data-ttu-id="018aa-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="018aa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018aa-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018aa-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018aa-145">입력</span><span class="sxs-lookup"><span data-stu-id="018aa-145">INPUTS</span></span>

### <span data-ttu-id="018aa-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="018aa-146">System.String</span></span>

### <span data-ttu-id="018aa-147">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="018aa-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="018aa-148">시스템 Null 허용 ' 1 [[NamespaceState, [Microsoft Azure. 1.3.0.0., Microsoft Azure. PowerShell, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="018aa-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="018aa-149">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="018aa-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="018aa-150">출력</span><span class="sxs-lookup"><span data-stu-id="018aa-150">OUTPUTS</span></span>

### <span data-ttu-id="018aa-151">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="018aa-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="018aa-152">상속자</span><span class="sxs-lookup"><span data-stu-id="018aa-152">NOTES</span></span>

## <span data-ttu-id="018aa-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="018aa-153">RELATED LINKS</span></span>
