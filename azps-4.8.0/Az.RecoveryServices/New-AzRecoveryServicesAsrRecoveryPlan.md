---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048071"
---
# <span data-ttu-id="b5c77-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5c77-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b5c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c77-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c77-103">ASR 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="b5c77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5c77-104">SYNTAX</span></span>

### <span data-ttu-id="b5c77-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="b5c77-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c77-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b5c77-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c77-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b5c77-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c77-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b5c77-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c77-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b5c77-109">DESCRIPTION</span></span>
<span data-ttu-id="b5c77-110">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet은 복구 서비스 자격 증명 모음에서 Azure Site recovery, 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="b5c77-111">복구 계획은 응용 프로그램에 속하는 가상 컴퓨터를 하나의 단위로 수집 하 여 함께 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="b5c77-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b5c77-112">EXAMPLES</span></span>

### <span data-ttu-id="b5c77-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5c77-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b5c77-114">지정 된 매개 변수를 사용 하 여 복구 계획 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b5c77-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b5c77-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b5c77-116">Azure zone에 대 한 복구 계획 만들기 작업을 영역 복제 된 항목으로 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b5c77-117">변수</span><span class="sxs-lookup"><span data-stu-id="b5c77-117">PARAMETERS</span></span>

### <span data-ttu-id="b5c77-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="b5c77-118">-Azure</span></span>
<span data-ttu-id="b5c77-119">Switch 매개 변수 azure에서 azure 재해 복구, 복구 계획 만들기에 대 한 시나리오를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="b5c77-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b5c77-120">-AzureZoneToZone</span></span>
<span data-ttu-id="b5c77-121">Switch 매개 변수 azure zone에서 영역 시나리오에 대 한 복제 된 항목 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="b5c77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c77-122">-DefaultProfile</span></span>
<span data-ttu-id="b5c77-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b5c77-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b5c77-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="b5c77-125">이 복구 계획에 포함 될 복제 보호 된 항목의 장애 조치 (failover) 배포 모델 (클래식 또는 리소스 관리자)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b5c77-126">-Name</span></span>
<span data-ttu-id="b5c77-127">복구 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-128">-Path</span><span class="sxs-lookup"><span data-stu-id="b5c77-128">-Path</span></span>
<span data-ttu-id="b5c77-129">복구 계획 정의 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="b5c77-130">복구 계획 정의 json을 사용 하 여 복구 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b5c77-131">-PrimaryFabric</span></span>
<span data-ttu-id="b5c77-132">이 복구 계획에 포함 될 복제 보호 된 항목의 주 ASR 패브릭에 대 한 ASR 패브릭 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="b5c77-133">-PrimaryZone</span></span>
<span data-ttu-id="b5c77-134">이 복구 계획에 포함 될 복제 보호 된 항목의 기본 Availabilty 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b5c77-135">-RecoveryFabric</span></span>
<span data-ttu-id="b5c77-136">이 복구 계획에 포함 될 복제 보호 된 항목의 복구 ASR 패브릭에 대 한 ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="b5c77-137">-RecoveryZone</span></span>
<span data-ttu-id="b5c77-138">이 복구 계획에 포함 될 복제 보호 된 항목의 기본 Availabilty 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5c77-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b5c77-140">복구 계획의 첫 번째 그룹에 추가할 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="b5c77-141">-확인</span><span class="sxs-lookup"><span data-stu-id="b5c77-141">-Confirm</span></span>
<span data-ttu-id="b5c77-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c77-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c77-143">-WhatIf</span></span>
<span data-ttu-id="b5c77-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5c77-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c77-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c77-146">CommonParameters</span></span>
<span data-ttu-id="b5c77-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c77-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c77-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5c77-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c77-149">입력</span><span class="sxs-lookup"><span data-stu-id="b5c77-149">INPUTS</span></span>

### <span data-ttu-id="b5c77-150">SiteRecovery. ASRReplicationProtectedItem []/.</span><span class="sxs-lookup"><span data-stu-id="b5c77-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="b5c77-151">출력</span><span class="sxs-lookup"><span data-stu-id="b5c77-151">OUTPUTS</span></span>

### <span data-ttu-id="b5c77-152">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="b5c77-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5c77-153">상속자</span><span class="sxs-lookup"><span data-stu-id="b5c77-153">NOTES</span></span>

## <span data-ttu-id="b5c77-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5c77-154">RELATED LINKS</span></span>

[<span data-ttu-id="b5c77-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5c77-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b5c77-156">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5c77-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b5c77-157">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5c77-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


