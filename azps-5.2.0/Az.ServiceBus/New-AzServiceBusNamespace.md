---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345465"
---
# <span data-ttu-id="91511-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="91511-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="91511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91511-102">SYNOPSIS</span></span>
<span data-ttu-id="91511-103">새 Service Bus 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="91511-104">구문</span><span class="sxs-lookup"><span data-stu-id="91511-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91511-105">설명</span><span class="sxs-lookup"><span data-stu-id="91511-105">DESCRIPTION</span></span>
<span data-ttu-id="91511-106">**New-AzServiceBusNamespace** cmdlet은 새 Service Bus 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="91511-107">네임스페이스 리소스 매니페스트를 만들면 변경이 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="91511-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="91511-108">이 작업은 idempotent입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-108">This operation is idempotent.</span></span>

## <span data-ttu-id="91511-109">예제</span><span class="sxs-lookup"><span data-stu-id="91511-109">EXAMPLES</span></span>

### <span data-ttu-id="91511-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91511-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="91511-111">지정된 리소스 그룹 내에서 새 Service Bus 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="91511-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91511-112">PARAMETERS</span></span>

### <span data-ttu-id="91511-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91511-113">-DefaultProfile</span></span>
<span data-ttu-id="91511-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91511-115">-Location</span><span class="sxs-lookup"><span data-stu-id="91511-115">-Location</span></span>
<span data-ttu-id="91511-116">Service Bus 네임스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="91511-117">-Name</span><span class="sxs-lookup"><span data-stu-id="91511-117">-Name</span></span>
<span data-ttu-id="91511-118">ServiceBus 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="91511-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91511-119">-ResourceGroupName</span></span>
<span data-ttu-id="91511-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-120">The resource group name.</span></span>

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

### <span data-ttu-id="91511-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="91511-121">-SkuCapacity</span></span>
<span data-ttu-id="91511-122">Service Bus 프리미엄 네임스페이스의 작업당 단위(허용되는 값 1 또는 2 또는 4)</span><span class="sxs-lookup"><span data-stu-id="91511-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="91511-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="91511-123">-SkuName</span></span>
<span data-ttu-id="91511-124">Service Bus 네임스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="91511-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="91511-125">-Tag</span></span>
<span data-ttu-id="91511-126">서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="91511-127">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="91511-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="91511-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91511-128">-Confirm</span></span>
<span data-ttu-id="91511-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91511-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91511-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91511-130">-WhatIf</span></span>
<span data-ttu-id="91511-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="91511-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91511-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91511-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91511-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91511-133">CommonParameters</span></span>
<span data-ttu-id="91511-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91511-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91511-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91511-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91511-136">입력</span><span class="sxs-lookup"><span data-stu-id="91511-136">INPUTS</span></span>

### <span data-ttu-id="91511-137">System.String</span><span class="sxs-lookup"><span data-stu-id="91511-137">System.String</span></span>

### <span data-ttu-id="91511-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91511-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91511-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="91511-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91511-140">출력</span><span class="sxs-lookup"><span data-stu-id="91511-140">OUTPUTS</span></span>

### <span data-ttu-id="91511-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="91511-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="91511-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91511-142">NOTES</span></span>

## <span data-ttu-id="91511-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91511-143">RELATED LINKS</span></span>
