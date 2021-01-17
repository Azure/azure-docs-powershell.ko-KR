---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494830"
---
# <span data-ttu-id="b96f7-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b96f7-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="b96f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b96f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b96f7-103">기존 Service Bus 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="b96f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b96f7-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96f7-105">설명</span><span class="sxs-lookup"><span data-stu-id="b96f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b96f7-106">**Set-AzServiceBusNamespace** cmdlet은 리소스 그룹 내에서 지정된 Service Bus 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="b96f7-107">예제</span><span class="sxs-lookup"><span data-stu-id="b96f7-107">EXAMPLES</span></span>

### <span data-ttu-id="b96f7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b96f7-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="b96f7-109">새 설명으로 Service Bus 네임스페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="b96f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b96f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b96f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96f7-111">-DefaultProfile</span></span>
<span data-ttu-id="b96f7-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b96f7-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b96f7-113">-Location</span></span>
<span data-ttu-id="b96f7-114">Service Bus 네임스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-114">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b96f7-115">-Name</span></span>
<span data-ttu-id="b96f7-116">ServiceBus 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b96f7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b96f7-119">-SkuCapacity</span></span>
<span data-ttu-id="b96f7-120">네임스페이스 SKU 용량.</span><span class="sxs-lookup"><span data-stu-id="b96f7-120">Namespace Sku Capacity.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b96f7-121">-SkuName</span></span>
<span data-ttu-id="b96f7-122">네임스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-122">The namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="b96f7-123">-Tag</span></span>
<span data-ttu-id="b96f7-124">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b96f7-125">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b96f7-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b96f7-126">-Confirm</span></span>
<span data-ttu-id="b96f7-127">지정된 정보로 Service Bus 네임스페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-127">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96f7-128">-WhatIf</span></span>
<span data-ttu-id="b96f7-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b96f7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b96f7-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96f7-131">CommonParameters</span></span>
<span data-ttu-id="b96f7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b96f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96f7-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b96f7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96f7-134">입력</span><span class="sxs-lookup"><span data-stu-id="b96f7-134">INPUTS</span></span>

### <span data-ttu-id="b96f7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b96f7-135">System.String</span></span>

### <span data-ttu-id="b96f7-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b96f7-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b96f7-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b96f7-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b96f7-138">출력</span><span class="sxs-lookup"><span data-stu-id="b96f7-138">OUTPUTS</span></span>

### <span data-ttu-id="b96f7-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b96f7-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b96f7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b96f7-140">NOTES</span></span>

## <span data-ttu-id="b96f7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b96f7-141">RELATED LINKS</span></span>
