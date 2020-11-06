---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: e2ac72ba5d563b4be902d424ad30c19b40bff9d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526183"
---
# <span data-ttu-id="2b0e2-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b0e2-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="2b0e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0e2-103">새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="2b0e2-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b0e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b0e2-104">SYNTAX</span></span>

### <span data-ttu-id="2b0e2-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b0e2-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b0e2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b0e2-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b0e2-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b0e2-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b0e2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b0e2-108">DESCRIPTION</span></span>
<span data-ttu-id="2b0e2-109">**AzureRmEventHubGeoDRConfiguration** cmdlet은 새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="2b0e2-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2b0e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b0e2-110">EXAMPLES</span></span>

### <span data-ttu-id="2b0e2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b0e2-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="2b0e2-112">기본 네임 스페이스가 "SampleNamespace_Primary" 인 "Sampledrcon.gif 이름"을 보조 네임 스페이스 "SampleNamespace_Secondary"로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2b0e2-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b0e2-113">PARAMETERS</span></span>

### <span data-ttu-id="2b0e2-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2b0e2-114">-AlternateName</span></span>
<span data-ttu-id="2b0e2-115">DR 구성 이름이 기본 네임 스페이스와 같은 경우 AlternateName 필요 함</span><span class="sxs-lookup"><span data-stu-id="2b0e2-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="2b0e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b0e2-116">-AsJob</span></span>
<span data-ttu-id="2b0e2-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2b0e2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b0e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0e2-118">-DefaultProfile</span></span>
<span data-ttu-id="2b0e2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b0e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b0e2-120">-InputObject</span></span>
<span data-ttu-id="2b0e2-121">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="2b0e2-121">Namespace Object</span></span>

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

### <span data-ttu-id="2b0e2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2b0e2-122">-Name</span></span>
<span data-ttu-id="2b0e2-123">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="2b0e2-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="2b0e2-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b0e2-124">-Namespace</span></span>
<span data-ttu-id="2b0e2-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2b0e2-125">Namespace Name</span></span>

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

### <span data-ttu-id="2b0e2-126">-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="2b0e2-126">-PartnerNamespace</span></span>
<span data-ttu-id="2b0e2-127">DR 구성 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="2b0e2-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="2b0e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b0e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b0e2-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2b0e2-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2b0e2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b0e2-130">-ResourceId</span></span>
<span data-ttu-id="2b0e2-131">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="2b0e2-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2b0e2-132">-확인</span><span class="sxs-lookup"><span data-stu-id="2b0e2-132">-Confirm</span></span>
<span data-ttu-id="2b0e2-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b0e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b0e2-134">-WhatIf</span></span>
<span data-ttu-id="2b0e2-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b0e2-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b0e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0e2-137">CommonParameters</span></span>
<span data-ttu-id="2b0e2-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0e2-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b0e2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0e2-140">입력</span><span class="sxs-lookup"><span data-stu-id="2b0e2-140">INPUTS</span></span>

### <span data-ttu-id="2b0e2-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b0e2-141">System.String</span></span>

### <span data-ttu-id="2b0e2-142">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="2b0e2-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="2b0e2-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2b0e2-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2b0e2-144">출력</span><span class="sxs-lookup"><span data-stu-id="2b0e2-144">OUTPUTS</span></span>

### <span data-ttu-id="2b0e2-145">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="2b0e2-145">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="2b0e2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="2b0e2-146">NOTES</span></span>

## <span data-ttu-id="2b0e2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b0e2-147">RELATED LINKS</span></span>
