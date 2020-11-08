---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: fe0d8f29650498e895e19e18bcb080107b2dbf35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218675"
---
# <span data-ttu-id="98076-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="98076-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="98076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98076-102">SYNOPSIS</span></span>
<span data-ttu-id="98076-103">새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="98076-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="98076-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98076-104">SYNTAX</span></span>

### <span data-ttu-id="98076-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="98076-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98076-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="98076-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98076-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98076-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98076-108">설명은</span><span class="sxs-lookup"><span data-stu-id="98076-108">DESCRIPTION</span></span>
<span data-ttu-id="98076-109">**AzEventHubGeoDRConfiguration** cmdlet은 새 별칭을 만듭니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="98076-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="98076-110">예제의</span><span class="sxs-lookup"><span data-stu-id="98076-110">EXAMPLES</span></span>

### <span data-ttu-id="98076-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="98076-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="98076-112">보조 네임 스페이스가 "SampleNamespace_Primary" 인 "SampleDRConfigName" 별칭을 만듭니다. "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="98076-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="98076-113">변수</span><span class="sxs-lookup"><span data-stu-id="98076-113">PARAMETERS</span></span>

### <span data-ttu-id="98076-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="98076-114">-AlternateName</span></span>
<span data-ttu-id="98076-115">DR 구성 이름이 기본 네임 스페이스와 같은 경우 AlternateName 필요 함</span><span class="sxs-lookup"><span data-stu-id="98076-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="98076-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98076-116">-AsJob</span></span>
<span data-ttu-id="98076-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="98076-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98076-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98076-118">-DefaultProfile</span></span>
<span data-ttu-id="98076-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98076-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98076-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98076-120">-InputObject</span></span>
<span data-ttu-id="98076-121">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="98076-121">Namespace Object</span></span>

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

### <span data-ttu-id="98076-122">-이름</span><span class="sxs-lookup"><span data-stu-id="98076-122">-Name</span></span>
<span data-ttu-id="98076-123">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="98076-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="98076-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98076-124">-Namespace</span></span>
<span data-ttu-id="98076-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="98076-125">Namespace Name</span></span>

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

### <span data-ttu-id="98076-126">-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="98076-126">-PartnerNamespace</span></span>
<span data-ttu-id="98076-127">DR 구성 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="98076-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="98076-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98076-128">-ResourceGroupName</span></span>
<span data-ttu-id="98076-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="98076-129">Resource Group Name</span></span>

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

### <span data-ttu-id="98076-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98076-130">-ResourceId</span></span>
<span data-ttu-id="98076-131">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="98076-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="98076-132">-확인</span><span class="sxs-lookup"><span data-stu-id="98076-132">-Confirm</span></span>
<span data-ttu-id="98076-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98076-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98076-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98076-134">-WhatIf</span></span>
<span data-ttu-id="98076-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="98076-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98076-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98076-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98076-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98076-137">CommonParameters</span></span>
<span data-ttu-id="98076-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98076-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98076-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98076-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98076-140">입력</span><span class="sxs-lookup"><span data-stu-id="98076-140">INPUTS</span></span>

### <span data-ttu-id="98076-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98076-141">System.String</span></span>

### <span data-ttu-id="98076-142">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="98076-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="98076-143">출력</span><span class="sxs-lookup"><span data-stu-id="98076-143">OUTPUTS</span></span>

### <span data-ttu-id="98076-144">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="98076-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="98076-145">상속자</span><span class="sxs-lookup"><span data-stu-id="98076-145">NOTES</span></span>

## <span data-ttu-id="98076-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98076-146">RELATED LINKS</span></span>
