---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: f06635819979823bbbdd298d3873c45ac0a5621a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982304"
---
# <span data-ttu-id="c3f82-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c3f82-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c3f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3f82-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f82-103">두 네트워크 간에 ASR 네트워크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="c3f82-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3f82-104">SYNTAX</span></span>

### <span data-ttu-id="c3f82-105">EnterpriseToEnterprise(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3f82-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3f82-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c3f82-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f82-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c3f82-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3f82-108">설명</span><span class="sxs-lookup"><span data-stu-id="c3f82-108">DESCRIPTION</span></span>
<span data-ttu-id="c3f82-109">**New-AzRecoveryServicesAsrNetworkMapping** cmdlet은 두 네트워크 간에 ASR 네트워크 매핑을 만드는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업에 대한 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c3f82-110">예제</span><span class="sxs-lookup"><span data-stu-id="c3f82-110">EXAMPLES</span></span>

### <span data-ttu-id="c3f82-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3f82-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="c3f82-112">지정된 이름, 기본 및 복구 네트워크를 사용하여 네트워크 매핑 만들기 작업을 시작하고 작업을 추적하기 위해 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="c3f82-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3f82-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="c3f82-114">지정된 이름, 기본 및 복구 네트워크를 사용하여 만들기 작업에 대한 네트워크 매핑을 시작하고 작업을 추적하는 ASR 작업을 반환합니다(Azure에서 Azure 시나리오).</span><span class="sxs-lookup"><span data-stu-id="c3f82-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="c3f82-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c3f82-115">PARAMETERS</span></span>

### <span data-ttu-id="c3f82-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c3f82-116">-AzureToAzure</span></span>
<span data-ttu-id="c3f82-117">플래그를 지정하여 AzureToAzure 시나리오를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f82-118">-DefaultProfile</span></span>
<span data-ttu-id="c3f82-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c3f82-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3f82-120">-Name</span></span>
<span data-ttu-id="c3f82-121">만들 ASR 네트워크 매핑의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-121">Name of the ASR network mapping to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3f82-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="c3f82-123">매핑에 대한 기본 네트워크의 Azure 가상 네트워크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="c3f82-124">-PrimaryFabric</span></span>
<span data-ttu-id="c3f82-125">매핑을 만들어야 하는 ASR 패브릭을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c3f82-126">-PrimaryNetwork</span></span>
<span data-ttu-id="c3f82-127">ASR 네트워크 매핑에 대한 기본 네트워크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3f82-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="c3f82-129">네트워크 매핑에 대한 복구 Azure 네트워크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="c3f82-130">-RecoveryFabric</span></span>
<span data-ttu-id="c3f82-131">복구 Azure 지역에 해당하는 Azure Site Recovery 패브릭 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c3f82-132">-RecoveryNetwork</span></span>
<span data-ttu-id="c3f82-133">ASR 네트워크 매핑에 대한 복구 네트워크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f82-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c3f82-134">-Confirm</span></span>
<span data-ttu-id="c3f82-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f82-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f82-136">-WhatIf</span></span>
<span data-ttu-id="c3f82-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3f82-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f82-139">CommonParameters</span></span>
<span data-ttu-id="c3f82-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f82-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3f82-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f82-142">입력</span><span class="sxs-lookup"><span data-stu-id="c3f82-142">INPUTS</span></span>

### <span data-ttu-id="c3f82-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c3f82-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c3f82-144">출력</span><span class="sxs-lookup"><span data-stu-id="c3f82-144">OUTPUTS</span></span>

### <span data-ttu-id="c3f82-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c3f82-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c3f82-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3f82-146">NOTES</span></span>

## <span data-ttu-id="c3f82-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3f82-147">RELATED LINKS</span></span>

[<span data-ttu-id="c3f82-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c3f82-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c3f82-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c3f82-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
