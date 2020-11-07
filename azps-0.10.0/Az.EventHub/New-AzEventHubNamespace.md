---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 592af2c1ecd26e3e744845ae24e8f9c71cf0b0f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875918"
---
# <span data-ttu-id="0fe6e-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0fe6e-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="0fe6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe6e-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe6e-103">이벤트 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="0fe6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fe6e-104">SYNTAX</span></span>

### <span data-ttu-id="0fe6e-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0fe6e-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe6e-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe6e-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe6e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0fe6e-107">DESCRIPTION</span></span>
<span data-ttu-id="0fe6e-108">New-AzEventHubNamespace cmdlet은 이벤트 허브 유형의 새 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="0fe6e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0fe6e-109">EXAMPLES</span></span>

### <span data-ttu-id="0fe6e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fe6e-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="0fe6e-111">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Mylocation에 이벤트 \` 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="0fe6e-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0fe6e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="0fe6e-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="0fe6e-113">\`지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만들고 \` \` \` , 리소스 그룹 \` MyResourceGroupName에서 \` MaximumThroughputUnits 10으로 autoinflate을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="0fe6e-114">예제 3-Kafka 사용 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="0fe6e-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="0fe6e-115">\` \` \` \` \` Kafka 및 autoinflate을 사용 하는 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="0fe6e-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="0fe6e-116">변수</span><span class="sxs-lookup"><span data-stu-id="0fe6e-116">PARAMETERS</span></span>

### <span data-ttu-id="0fe6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe6e-117">-DefaultProfile</span></span>
<span data-ttu-id="0fe6e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe6e-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="0fe6e-119">-EnableAutoInflate</span></span>
<span data-ttu-id="0fe6e-120">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="0fe6e-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="0fe6e-121">-EnableKafka</span></span>
<span data-ttu-id="0fe6e-122">네임 스페이스의 Kafka을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="0fe6e-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="0fe6e-123">-위치</span><span class="sxs-lookup"><span data-stu-id="0fe6e-123">-Location</span></span>
<span data-ttu-id="0fe6e-124">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="0fe6e-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="0fe6e-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="0fe6e-126">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="0fe6e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="0fe6e-127">-Name</span></span>
<span data-ttu-id="0fe6e-128">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="0fe6e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe6e-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fe6e-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0fe6e-130">Resource Group Name</span></span>

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

### <span data-ttu-id="0fe6e-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0fe6e-131">-SkuCapacity</span></span>
<span data-ttu-id="0fe6e-132">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="0fe6e-133">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="0fe6e-133">-SkuName</span></span>
<span data-ttu-id="0fe6e-134">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="0fe6e-135">태그</span><span class="sxs-lookup"><span data-stu-id="0fe6e-135">-Tag</span></span>
<span data-ttu-id="0fe6e-136">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="0fe6e-137">-확인</span><span class="sxs-lookup"><span data-stu-id="0fe6e-137">-Confirm</span></span>
<span data-ttu-id="0fe6e-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe6e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe6e-139">-WhatIf</span></span>
<span data-ttu-id="0fe6e-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe6e-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe6e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe6e-142">CommonParameters</span></span>
<span data-ttu-id="0fe6e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe6e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe6e-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe6e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe6e-145">입력</span><span class="sxs-lookup"><span data-stu-id="0fe6e-145">INPUTS</span></span>

### <span data-ttu-id="0fe6e-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0fe6e-146">System.String</span></span>

### <span data-ttu-id="0fe6e-147">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="0fe6e-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0fe6e-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0fe6e-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0fe6e-149">출력</span><span class="sxs-lookup"><span data-stu-id="0fe6e-149">OUTPUTS</span></span>

### <span data-ttu-id="0fe6e-150">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="0fe6e-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0fe6e-151">상속자</span><span class="sxs-lookup"><span data-stu-id="0fe6e-151">NOTES</span></span>

## <span data-ttu-id="0fe6e-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fe6e-152">RELATED LINKS</span></span>
