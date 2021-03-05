---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985693"
---
# <span data-ttu-id="56619-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56619-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="56619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56619-102">SYNOPSIS</span></span>
<span data-ttu-id="56619-103">ASR 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56619-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="56619-104">구문</span><span class="sxs-lookup"><span data-stu-id="56619-104">SYNTAX</span></span>

### <span data-ttu-id="56619-105">EnterpriseToEnterprise(기본값)</span><span class="sxs-lookup"><span data-stu-id="56619-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56619-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="56619-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56619-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="56619-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56619-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="56619-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56619-109">설명</span><span class="sxs-lookup"><span data-stu-id="56619-109">DESCRIPTION</span></span>
<span data-ttu-id="56619-110">**New-AzRecoveryServicesAsrRecoveryPlan** cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery, 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56619-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="56619-111">복구 계획은 애플리케이션에 속한 가상 머신을 한 단위로 수집하여 함께 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="56619-112">예제</span><span class="sxs-lookup"><span data-stu-id="56619-112">EXAMPLES</span></span>

### <span data-ttu-id="56619-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="56619-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="56619-114">지정된 매개 변수로 복구 계획 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="56619-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="56619-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="56619-116">복제된 항목을 영역으로 Azure 영역의 복구 계획 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="56619-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56619-117">PARAMETERS</span></span>

### <span data-ttu-id="56619-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="56619-118">-Azure</span></span>
<span data-ttu-id="56619-119">스위치 매개 변수는 Azure에 대한 시나리오를 azure 재해 복구, 복구 계획 만들기로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="56619-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="56619-120">-AzureZoneToZone</span></span>
<span data-ttu-id="56619-121">스위치 매개 변수는 azure 영역의 복제된 항목을 영역 시나리오로 만드는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="56619-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56619-122">-DefaultProfile</span></span>
<span data-ttu-id="56619-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56619-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="56619-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="56619-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="56619-125">이 복구 계획의 일부가 될 복제 보호 항목의 장애 조치(failover) 배포 모델(클래식 또는 리소스 관리자)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="56619-126">-Name</span><span class="sxs-lookup"><span data-stu-id="56619-126">-Name</span></span>
<span data-ttu-id="56619-127">복구 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56619-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="56619-128">-Path</span><span class="sxs-lookup"><span data-stu-id="56619-128">-Path</span></span>
<span data-ttu-id="56619-129">복구 계획 정의 json 파일에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="56619-130">복구 계획 정의 json을 사용하여 복구 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56619-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="56619-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="56619-131">-PrimaryFabric</span></span>
<span data-ttu-id="56619-132">이 복구 계획의 일부가 될 복제 보호 항목의 기본 ASR 패브릭에 대한 ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="56619-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="56619-133">-PrimaryZone</span></span>
<span data-ttu-id="56619-134">이 복구 계획의 일부가 될 복제 보호 항목의 기본 Availabilty 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="56619-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="56619-135">-RecoveryFabric</span></span>
<span data-ttu-id="56619-136">이 복구 계획의 일부가 될 복제 보호 항목의 복구 ASR 패브릭에 대한 ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="56619-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="56619-137">-RecoveryZone</span></span>
<span data-ttu-id="56619-138">이 복구 계획의 일부가 될 복제 보호 항목의 기본 Availabilty 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="56619-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56619-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="56619-140">복구 계획의 첫 번째 그룹에 추가할 복제 보호 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="56619-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="56619-141">-확인</span><span class="sxs-lookup"><span data-stu-id="56619-141">-Confirm</span></span>
<span data-ttu-id="56619-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="56619-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56619-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56619-143">-WhatIf</span></span>
<span data-ttu-id="56619-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="56619-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56619-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56619-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56619-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56619-146">CommonParameters</span></span>
<span data-ttu-id="56619-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56619-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56619-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56619-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56619-149">입력</span><span class="sxs-lookup"><span data-stu-id="56619-149">INPUTS</span></span>

### <span data-ttu-id="56619-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="56619-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="56619-151">출력</span><span class="sxs-lookup"><span data-stu-id="56619-151">OUTPUTS</span></span>

### <span data-ttu-id="56619-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="56619-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56619-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56619-153">NOTES</span></span>

## <span data-ttu-id="56619-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56619-154">RELATED LINKS</span></span>

[<span data-ttu-id="56619-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56619-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="56619-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56619-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="56619-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56619-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


