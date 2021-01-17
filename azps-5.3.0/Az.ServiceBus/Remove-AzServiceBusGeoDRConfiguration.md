---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494855"
---
# <span data-ttu-id="d7fc6-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7fc6-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d7fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fc6-103">별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="d7fc6-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d7fc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7fc6-104">SYNTAX</span></span>

### <span data-ttu-id="d7fc6-105">GeoDRPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7fc6-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fc6-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7fc6-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fc6-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7fc6-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7fc6-108">설명</span><span class="sxs-lookup"><span data-stu-id="d7fc6-108">DESCRIPTION</span></span>
<span data-ttu-id="d7fc6-109">**Remove-AzServiceBusGeoDRConfiguration** cmdlet은 별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="d7fc6-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d7fc6-110">예제</span><span class="sxs-lookup"><span data-stu-id="d7fc6-110">EXAMPLES</span></span>

### <span data-ttu-id="d7fc6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7fc6-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="d7fc6-112">별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="d7fc6-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d7fc6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7fc6-113">PARAMETERS</span></span>

### <span data-ttu-id="d7fc6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7fc6-114">-AsJob</span></span>
<span data-ttu-id="d7fc6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d7fc6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7fc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fc6-116">-DefaultProfile</span></span>
<span data-ttu-id="d7fc6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7fc6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7fc6-118">-InputObject</span></span>
<span data-ttu-id="d7fc6-119">Service Bus GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="d7fc6-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="d7fc6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d7fc6-120">-Name</span></span>
<span data-ttu-id="d7fc6-121">별칭(GeoDR) 이름</span><span class="sxs-lookup"><span data-stu-id="d7fc6-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="d7fc6-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7fc6-122">-Namespace</span></span>
<span data-ttu-id="d7fc6-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d7fc6-123">Namespace Name</span></span>

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

### <span data-ttu-id="d7fc6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7fc6-124">-PassThru</span></span>
<span data-ttu-id="d7fc6-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7fc6-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7fc6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7fc6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7fc6-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d7fc6-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d7fc6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7fc6-129">-ResourceId</span></span>
<span data-ttu-id="d7fc6-130">GeoDRConfiguration 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d7fc6-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="d7fc6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7fc6-131">-Confirm</span></span>
<span data-ttu-id="d7fc6-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7fc6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7fc6-133">-WhatIf</span></span>
<span data-ttu-id="d7fc6-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7fc6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7fc6-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7fc6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fc6-136">CommonParameters</span></span>
<span data-ttu-id="d7fc6-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fc6-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fc6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fc6-139">입력</span><span class="sxs-lookup"><span data-stu-id="d7fc6-139">INPUTS</span></span>

### <span data-ttu-id="d7fc6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d7fc6-140">System.String</span></span>

### <span data-ttu-id="d7fc6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d7fc6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d7fc6-142">출력</span><span class="sxs-lookup"><span data-stu-id="d7fc6-142">OUTPUTS</span></span>

### <span data-ttu-id="d7fc6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7fc6-143">System.Boolean</span></span>

## <span data-ttu-id="d7fc6-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7fc6-144">NOTES</span></span>

## <span data-ttu-id="d7fc6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7fc6-145">RELATED LINKS</span></span>
