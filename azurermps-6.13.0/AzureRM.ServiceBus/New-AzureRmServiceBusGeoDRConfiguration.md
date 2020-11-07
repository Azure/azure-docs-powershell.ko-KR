---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702894"
---
# <span data-ttu-id="d0197-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0197-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d0197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0197-102">SYNOPSIS</span></span>
<span data-ttu-id="d0197-103">새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="d0197-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0197-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0197-104">SYNTAX</span></span>

### <span data-ttu-id="d0197-105">Geodr속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0197-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0197-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0197-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0197-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0197-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0197-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d0197-108">DESCRIPTION</span></span>
<span data-ttu-id="d0197-109">**AzureRmServiceBusGeoDRConfiguration** cmdlet은 새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="d0197-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d0197-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d0197-110">EXAMPLES</span></span>

### <span data-ttu-id="d0197-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0197-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="d0197-112">기본 네임 스페이스가 "SampleNamespace_Primary" 인 "Sampledrcon.gif 이름"을 보조 네임 스페이스 "SampleNamespace_Secondary"로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="d0197-113">변수</span><span class="sxs-lookup"><span data-stu-id="d0197-113">PARAMETERS</span></span>

### <span data-ttu-id="d0197-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="d0197-114">-AlternateName</span></span>
<span data-ttu-id="d0197-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="d0197-115">AlternateName</span></span>

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

### <span data-ttu-id="d0197-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0197-116">-AsJob</span></span>
<span data-ttu-id="d0197-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d0197-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0197-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0197-118">-DefaultProfile</span></span>
<span data-ttu-id="d0197-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0197-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0197-120">-InputObject</span></span>
<span data-ttu-id="d0197-121">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="d0197-121">Namespace Object</span></span>

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

### <span data-ttu-id="d0197-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d0197-122">-Name</span></span>
<span data-ttu-id="d0197-123">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="d0197-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="d0197-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0197-124">-Namespace</span></span>
<span data-ttu-id="d0197-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d0197-125">Namespace Name</span></span>

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

### <span data-ttu-id="d0197-126">-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="d0197-126">-PartnerNamespace</span></span>
<span data-ttu-id="d0197-127">DR 구성 네임 스페이스 (이름 네임 스페이스의 ARM Id [보조 네임 스페이스])</span><span class="sxs-lookup"><span data-stu-id="d0197-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="d0197-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0197-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0197-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d0197-129">Resource Group Name</span></span>

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

### <span data-ttu-id="d0197-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0197-130">-ResourceId</span></span>
<span data-ttu-id="d0197-131">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d0197-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d0197-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d0197-132">-Confirm</span></span>
<span data-ttu-id="d0197-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0197-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0197-134">-WhatIf</span></span>
<span data-ttu-id="d0197-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0197-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0197-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0197-137">CommonParameters</span></span>
<span data-ttu-id="d0197-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0197-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0197-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0197-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0197-140">입력</span><span class="sxs-lookup"><span data-stu-id="d0197-140">INPUTS</span></span>

### <span data-ttu-id="d0197-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0197-141">System.String</span></span>

### <span data-ttu-id="d0197-142">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="d0197-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="d0197-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0197-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d0197-144">출력</span><span class="sxs-lookup"><span data-stu-id="d0197-144">OUTPUTS</span></span>

### <span data-ttu-id="d0197-145">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d0197-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d0197-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d0197-146">NOTES</span></span>

## <span data-ttu-id="d0197-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0197-147">RELATED LINKS</span></span>
