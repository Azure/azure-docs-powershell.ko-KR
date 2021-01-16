---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333290"
---
# <span data-ttu-id="f3c4e-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f3c4e-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f3c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c4e-103">ASR 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="f3c4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3c4e-104">SYNTAX</span></span>

### <span data-ttu-id="f3c4e-105">EnterpriseToEnterprise(기본값)</span><span class="sxs-lookup"><span data-stu-id="f3c4e-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c4e-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f3c4e-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c4e-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="f3c4e-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c4e-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="f3c4e-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c4e-109">설명</span><span class="sxs-lookup"><span data-stu-id="f3c4e-109">DESCRIPTION</span></span>
<span data-ttu-id="f3c4e-110">**New-AzRecoveryServicesAsrRecoveryPlan** cmdlet은 Recovery Services 자격 증명 모음에 Azure Site Recovery, 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="f3c4e-111">복구 계획은 애플리케이션에 속한 가상 머신을 한 단위로 수집하여 함께 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="f3c4e-112">예제</span><span class="sxs-lookup"><span data-stu-id="f3c4e-112">EXAMPLES</span></span>

### <span data-ttu-id="f3c4e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3c4e-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="f3c4e-114">지정된 매개 변수를 사용하여 복구 계획 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f3c4e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f3c4e-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="f3c4e-116">영역 복제 항목에 대한 Azure 영역의 복구 계획 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f3c4e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3c4e-117">PARAMETERS</span></span>

### <span data-ttu-id="f3c4e-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="f3c4e-118">-Azure</span></span>
<span data-ttu-id="f3c4e-119">스위치 매개 변수는 Azure에서 Azure 재해 복구, 복구 계획 만들기에 대한 시나리오를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="f3c4e-120">-AzureZoneToZone</span></span>
<span data-ttu-id="f3c4e-121">스위치 매개 변수는 Azure 영역의 복제된 항목 만들기를 영역 시나리오로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c4e-122">-DefaultProfile</span></span>
<span data-ttu-id="f3c4e-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3c4e-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="f3c4e-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="f3c4e-125">이 복구 계획의 일부가 될 복제 보호 항목의 장애 조치 배포 모델(클래식 또는 Resource Manager)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c4e-126">-Name</span></span>
<span data-ttu-id="f3c4e-127">복구 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-128">-Path</span><span class="sxs-lookup"><span data-stu-id="f3c4e-128">-Path</span></span>
<span data-ttu-id="f3c4e-129">복구 계획 정의 json 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="f3c4e-130">복구 계획 정의 json을 사용하여 복구 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="f3c4e-131">-PrimaryFabric</span></span>
<span data-ttu-id="f3c4e-132">이 복구 계획의 일부가 될 복제 보호 항목의 기본 ASR 패브릭에 대한 ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="f3c4e-133">-PrimaryZone</span></span>
<span data-ttu-id="f3c4e-134">이 복구 계획의 일부가 될 복제 보호된 항목의 기본 사용이이상 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="f3c4e-135">-RecoveryFabric</span></span>
<span data-ttu-id="f3c4e-136">이 복구 계획의 일부가 될 복제 보호 항목의 복구 ASR 패브릭에 대한 ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="f3c4e-137">-RecoveryZone</span></span>
<span data-ttu-id="f3c4e-138">이 복구 계획의 일부가 될 복제 보호된 항목의 기본 사용이이상 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f3c4e-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f3c4e-140">복구 계획의 첫 번째 그룹에 추가할 복제 보호 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c4e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3c4e-141">-Confirm</span></span>
<span data-ttu-id="f3c4e-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c4e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c4e-143">-WhatIf</span></span>
<span data-ttu-id="f3c4e-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3c4e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3c4e-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c4e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c4e-146">CommonParameters</span></span>
<span data-ttu-id="f3c4e-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c4e-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3c4e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c4e-149">입력</span><span class="sxs-lookup"><span data-stu-id="f3c4e-149">INPUTS</span></span>

### <span data-ttu-id="f3c4e-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="f3c4e-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="f3c4e-151">출력</span><span class="sxs-lookup"><span data-stu-id="f3c4e-151">OUTPUTS</span></span>

### <span data-ttu-id="f3c4e-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3c4e-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3c4e-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3c4e-153">NOTES</span></span>

## <span data-ttu-id="f3c4e-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3c4e-154">RELATED LINKS</span></span>

[<span data-ttu-id="f3c4e-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f3c4e-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f3c4e-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f3c4e-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f3c4e-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f3c4e-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


