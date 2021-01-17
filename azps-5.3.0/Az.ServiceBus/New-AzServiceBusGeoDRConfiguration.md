---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494872"
---
# <span data-ttu-id="6fb15-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fb15-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="6fb15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb15-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb15-103">새 별칭을 만듭니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="6fb15-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6fb15-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fb15-104">SYNTAX</span></span>

### <span data-ttu-id="6fb15-105">GeoDRPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6fb15-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb15-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fb15-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb15-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb15-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fb15-108">설명</span><span class="sxs-lookup"><span data-stu-id="6fb15-108">DESCRIPTION</span></span>
<span data-ttu-id="6fb15-109">**New-AzServiceBusGeoDRConfiguration** cmdlet은 새 별칭을 만듭니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="6fb15-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6fb15-110">예제</span><span class="sxs-lookup"><span data-stu-id="6fb15-110">EXAMPLES</span></span>

### <span data-ttu-id="6fb15-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fb15-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="6fb15-112">보조 네임스페이스 "SampleNamespace_Primary" 기본 네임스페이스가 있는 "SampleDRConfigName" 별칭을 만듭니다SampleNamespace_Secondary</span><span class="sxs-lookup"><span data-stu-id="6fb15-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="6fb15-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fb15-113">PARAMETERS</span></span>

### <span data-ttu-id="6fb15-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="6fb15-114">-AlternateName</span></span>
<span data-ttu-id="6fb15-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="6fb15-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb15-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fb15-116">-AsJob</span></span>
<span data-ttu-id="6fb15-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6fb15-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fb15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb15-118">-DefaultProfile</span></span>
<span data-ttu-id="6fb15-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fb15-120">-InputObject</span></span>
<span data-ttu-id="6fb15-121">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="6fb15-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb15-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6fb15-122">-Name</span></span>
<span data-ttu-id="6fb15-123">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="6fb15-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="6fb15-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6fb15-124">-Namespace</span></span>
<span data-ttu-id="6fb15-125">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6fb15-125">Namespace Name</span></span>

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

### <span data-ttu-id="6fb15-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="6fb15-126">-PartnerNamespace</span></span>
<span data-ttu-id="6fb15-127">DR 구성 PartnerNamespace(ARM PartnerNamespace [보조 네임스페이스]의 ID)</span><span class="sxs-lookup"><span data-stu-id="6fb15-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb15-128">-ResourceGroupName</span></span>
<span data-ttu-id="6fb15-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6fb15-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6fb15-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb15-130">-ResourceId</span></span>
<span data-ttu-id="6fb15-131">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6fb15-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb15-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fb15-132">-Confirm</span></span>
<span data-ttu-id="6fb15-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fb15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb15-134">-WhatIf</span></span>
<span data-ttu-id="6fb15-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6fb15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fb15-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fb15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fb15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb15-137">CommonParameters</span></span>
<span data-ttu-id="6fb15-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb15-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6fb15-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb15-140">입력</span><span class="sxs-lookup"><span data-stu-id="6fb15-140">INPUTS</span></span>

### <span data-ttu-id="6fb15-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6fb15-141">System.String</span></span>

### <span data-ttu-id="6fb15-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6fb15-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6fb15-143">출력</span><span class="sxs-lookup"><span data-stu-id="6fb15-143">OUTPUTS</span></span>

### <span data-ttu-id="6fb15-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6fb15-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="6fb15-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fb15-145">NOTES</span></span>

## <span data-ttu-id="6fb15-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fb15-146">RELATED LINKS</span></span>
