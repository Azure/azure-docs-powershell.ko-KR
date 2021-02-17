---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 83d1e9edde6e2e792a24e0dc943cf62068938c2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196329"
---
# <span data-ttu-id="edca3-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="edca3-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="edca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edca3-102">SYNOPSIS</span></span>
<span data-ttu-id="edca3-103">새 별칭을 만듭니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="edca3-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="edca3-104">구문</span><span class="sxs-lookup"><span data-stu-id="edca3-104">SYNTAX</span></span>

### <span data-ttu-id="edca3-105">GeoDRParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="edca3-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edca3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="edca3-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edca3-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edca3-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edca3-108">설명</span><span class="sxs-lookup"><span data-stu-id="edca3-108">DESCRIPTION</span></span>
<span data-ttu-id="edca3-109">**New-AzEventHubGeoDRConfiguration** cmdlet은 새 별칭을 만듭니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="edca3-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="edca3-110">예제</span><span class="sxs-lookup"><span data-stu-id="edca3-110">EXAMPLES</span></span>

### <span data-ttu-id="edca3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="edca3-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="edca3-112">보조 네임스페이스 "SampleNamespace_Primary" 기본 네임스페이스가 있는 "SampleDRConfigName" 별칭을 만듭니다SampleNamespace_Secondary</span><span class="sxs-lookup"><span data-stu-id="edca3-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="edca3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edca3-113">PARAMETERS</span></span>

### <span data-ttu-id="edca3-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="edca3-114">-AlternateName</span></span>
<span data-ttu-id="edca3-115">DR 구성 이름이 기본 네임스페이스와 같은 경우 AlternateName 필요</span><span class="sxs-lookup"><span data-stu-id="edca3-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="edca3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edca3-116">-AsJob</span></span>
<span data-ttu-id="edca3-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="edca3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edca3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edca3-118">-DefaultProfile</span></span>
<span data-ttu-id="edca3-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edca3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edca3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edca3-120">-InputObject</span></span>
<span data-ttu-id="edca3-121">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="edca3-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edca3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="edca3-122">-Name</span></span>
<span data-ttu-id="edca3-123">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="edca3-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="edca3-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="edca3-124">-Namespace</span></span>
<span data-ttu-id="edca3-125">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="edca3-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edca3-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="edca3-126">-PartnerNamespace</span></span>
<span data-ttu-id="edca3-127">DR 구성 PartnerNamespace ARM ID</span><span class="sxs-lookup"><span data-stu-id="edca3-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="edca3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edca3-128">-ResourceGroupName</span></span>
<span data-ttu-id="edca3-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="edca3-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edca3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edca3-130">-ResourceId</span></span>
<span data-ttu-id="edca3-131">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="edca3-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="edca3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edca3-132">-Confirm</span></span>
<span data-ttu-id="edca3-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="edca3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edca3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edca3-134">-WhatIf</span></span>
<span data-ttu-id="edca3-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="edca3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edca3-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edca3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edca3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edca3-137">CommonParameters</span></span>
<span data-ttu-id="edca3-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edca3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edca3-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="edca3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edca3-140">입력</span><span class="sxs-lookup"><span data-stu-id="edca3-140">INPUTS</span></span>

### <span data-ttu-id="edca3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="edca3-141">System.String</span></span>

### <span data-ttu-id="edca3-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="edca3-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="edca3-143">출력</span><span class="sxs-lookup"><span data-stu-id="edca3-143">OUTPUTS</span></span>

### <span data-ttu-id="edca3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="edca3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="edca3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edca3-145">NOTES</span></span>

## <span data-ttu-id="edca3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edca3-146">RELATED LINKS</span></span>
