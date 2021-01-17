---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494831"
---
# <span data-ttu-id="dd716-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="dd716-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="dd716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd716-102">SYNOPSIS</span></span>
<span data-ttu-id="dd716-103">GEO DR 장애 조치(failover)를 호출하고 보조 네임스페이스를 지점으로 별칭을 다시 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="dd716-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd716-104">SYNTAX</span></span>

### <span data-ttu-id="dd716-105">GeoDRPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd716-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd716-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd716-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd716-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd716-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd716-108">설명</span><span class="sxs-lookup"><span data-stu-id="dd716-108">DESCRIPTION</span></span>
<span data-ttu-id="dd716-109">**Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet은 GEO DR 장애 조치(failover)를 호출하고 보조 네임스페이스를 지점으로 별칭을 다시 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="dd716-110">예제</span><span class="sxs-lookup"><span data-stu-id="dd716-110">EXAMPLES</span></span>

### <span data-ttu-id="dd716-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd716-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="dd716-112">별칭 "SampleDRConfigName"을 통해 장애 조치(Failover)를 호출하고, 다시 구성하고, 보조 네임스페이스 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="dd716-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="dd716-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd716-113">PARAMETERS</span></span>

### <span data-ttu-id="dd716-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd716-114">-DefaultProfile</span></span>
<span data-ttu-id="dd716-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd716-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd716-116">-InputObject</span></span>
<span data-ttu-id="dd716-117">Service Bus GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="dd716-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd716-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dd716-118">-Name</span></span>
<span data-ttu-id="dd716-119">DR 구성 이름 - 별칭</span><span class="sxs-lookup"><span data-stu-id="dd716-119">DR Configuration Name - Alias</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd716-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd716-120">-Namespace</span></span>
<span data-ttu-id="dd716-121">네임스페이스 이름 - 보조 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="dd716-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd716-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd716-122">-PassThru</span></span>
<span data-ttu-id="dd716-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd716-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd716-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd716-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd716-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dd716-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd716-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd716-127">-ResourceId</span></span>
<span data-ttu-id="dd716-128">GeoDRConfiguration 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dd716-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd716-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd716-129">-Confirm</span></span>
<span data-ttu-id="dd716-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd716-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd716-131">-WhatIf</span></span>
<span data-ttu-id="dd716-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dd716-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd716-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd716-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd716-134">CommonParameters</span></span>
<span data-ttu-id="dd716-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd716-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd716-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dd716-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd716-137">입력</span><span class="sxs-lookup"><span data-stu-id="dd716-137">INPUTS</span></span>

### <span data-ttu-id="dd716-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dd716-138">System.String</span></span>

### <span data-ttu-id="dd716-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dd716-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="dd716-140">출력</span><span class="sxs-lookup"><span data-stu-id="dd716-140">OUTPUTS</span></span>

### <span data-ttu-id="dd716-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd716-141">System.Boolean</span></span>

## <span data-ttu-id="dd716-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd716-142">NOTES</span></span>

## <span data-ttu-id="dd716-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd716-143">RELATED LINKS</span></span>
