---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5e0c3627616ae7310785943f73ed7c07f0f263b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872930"
---
# <span data-ttu-id="84d2e-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84d2e-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="84d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="84d2e-103">ASR 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="84d2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84d2e-104">SYNTAX</span></span>

### <span data-ttu-id="84d2e-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="84d2e-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d2e-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="84d2e-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d2e-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="84d2e-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d2e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="84d2e-108">DESCRIPTION</span></span>
<span data-ttu-id="84d2e-109">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="84d2e-110">복구 계획은 응용 프로그램에 속하는 가상 컴퓨터를 하나의 단위로 수집 하 여 함께 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="84d2e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="84d2e-111">EXAMPLES</span></span>

### <span data-ttu-id="84d2e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="84d2e-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="84d2e-113">지정 된 매개 변수를 사용 하 여 복구 계획 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="84d2e-114">변수</span><span class="sxs-lookup"><span data-stu-id="84d2e-114">PARAMETERS</span></span>

### <span data-ttu-id="84d2e-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="84d2e-115">-Azure</span></span>
<span data-ttu-id="84d2e-116">{{Azure 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="84d2e-116">{{Fill Azure Description}}</span></span>

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

### <span data-ttu-id="84d2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d2e-117">-DefaultProfile</span></span>
<span data-ttu-id="84d2e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="84d2e-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="84d2e-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="84d2e-120">이 복구 계획에 포함 될 복제 보호 된 항목의 장애 조치 (failover) 배포 모델 (클래식 또는 리소스 관리자)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="84d2e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="84d2e-121">-Name</span></span>
<span data-ttu-id="84d2e-122">복구 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d2e-123">-Path</span><span class="sxs-lookup"><span data-stu-id="84d2e-123">-Path</span></span>
<span data-ttu-id="84d2e-124">복구 계획 정의 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="84d2e-125">복구 계획 정의 json을 사용 하 여 복구 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="84d2e-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="84d2e-126">-PrimaryFabric</span></span>
<span data-ttu-id="84d2e-127">이 복구 계획에 포함 될 복제 보호 된 항목의 주 ASR 패브릭에 대 한 ASR 패브릭 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d2e-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="84d2e-128">-RecoveryFabric</span></span>
<span data-ttu-id="84d2e-129">이 복구 계획에 포함 될 복제 보호 된 항목의 복구 ASR 패브릭에 대 한 ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="84d2e-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84d2e-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="84d2e-131">복구 계획의 첫 번째 그룹에 추가할 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="84d2e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="84d2e-132">-Confirm</span></span>
<span data-ttu-id="84d2e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d2e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d2e-134">-WhatIf</span></span>
<span data-ttu-id="84d2e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84d2e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d2e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d2e-137">CommonParameters</span></span>
<span data-ttu-id="84d2e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d2e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d2e-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d2e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d2e-140">입력</span><span class="sxs-lookup"><span data-stu-id="84d2e-140">INPUTS</span></span>

### <span data-ttu-id="84d2e-141">SiteRecovery. ASRReplicationProtectedItem []/.</span><span class="sxs-lookup"><span data-stu-id="84d2e-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="84d2e-142">출력</span><span class="sxs-lookup"><span data-stu-id="84d2e-142">OUTPUTS</span></span>

### <span data-ttu-id="84d2e-143">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="84d2e-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84d2e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="84d2e-144">NOTES</span></span>

## <span data-ttu-id="84d2e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84d2e-145">RELATED LINKS</span></span>

[<span data-ttu-id="84d2e-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84d2e-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="84d2e-147">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84d2e-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="84d2e-148">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84d2e-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


