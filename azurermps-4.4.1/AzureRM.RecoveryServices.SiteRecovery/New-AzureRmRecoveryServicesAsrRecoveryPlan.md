---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702424"
---
# <span data-ttu-id="059a0-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="059a0-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="059a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059a0-102">SYNOPSIS</span></span>
<span data-ttu-id="059a0-103">ASR 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="059a0-104">SYNTAX</span></span>

### <span data-ttu-id="059a0-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="059a0-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="059a0-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="059a0-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059a0-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="059a0-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059a0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="059a0-108">DESCRIPTION</span></span>
<span data-ttu-id="059a0-109">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 복구 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="059a0-110">복구 계획은 응용 프로그램에 속하는 가상 컴퓨터를 하나의 단위로 수집 하 여 함께 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="059a0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="059a0-111">EXAMPLES</span></span>

### <span data-ttu-id="059a0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="059a0-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="059a0-113">지정 된 매개 변수를 사용 하 여 복구 계획 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="059a0-114">변수</span><span class="sxs-lookup"><span data-stu-id="059a0-114">PARAMETERS</span></span>

### <span data-ttu-id="059a0-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="059a0-115">-Azure</span></span>
<span data-ttu-id="059a0-116">복구 계획의 복구 위치를 Azure로 지정 하는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="059a0-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="059a0-118">이 복구 계획에 포함 될 복제 보호 된 항목의 장애 조치 (failover) 배포 모델 (클래식 또는 리소스 관리자)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="059a0-119">-Name</span></span>
<span data-ttu-id="059a0-120">복구 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-121">-Path</span><span class="sxs-lookup"><span data-stu-id="059a0-121">-Path</span></span>
<span data-ttu-id="059a0-122">복구 계획 정의 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="059a0-123">복구 계획 정의 json을 사용 하 여 복구 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="059a0-124">-PrimaryFabric</span></span>
<span data-ttu-id="059a0-125">이 복구 계획에 포함 될 복제 보호 된 항목의 주 ASR 패브릭에 대 한 ASR 패브릭 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="059a0-126">-RecoveryFabric</span></span>
<span data-ttu-id="059a0-127">이 복구 계획에 포함 될 복제 보호 된 항목의 복구 ASR 패브릭에 대 한 ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="059a0-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="059a0-129">복구 계획의 첫 번째 그룹에 추가할 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="059a0-130">-Confirm</span></span>
<span data-ttu-id="059a0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059a0-132">-WhatIf</span></span>
<span data-ttu-id="059a0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059a0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059a0-135">CommonParameters</span></span>
<span data-ttu-id="059a0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="059a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059a0-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059a0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059a0-138">입력</span><span class="sxs-lookup"><span data-stu-id="059a0-138">INPUTS</span></span>

### <span data-ttu-id="059a0-139">SiteRecovery. ASRReplicationProtectedItem []/.</span><span class="sxs-lookup"><span data-stu-id="059a0-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="059a0-140">출력</span><span class="sxs-lookup"><span data-stu-id="059a0-140">OUTPUTS</span></span>

### <span data-ttu-id="059a0-141">System. 개체</span><span class="sxs-lookup"><span data-stu-id="059a0-141">System.Object</span></span>

## <span data-ttu-id="059a0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="059a0-142">NOTES</span></span>

## <span data-ttu-id="059a0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059a0-143">RELATED LINKS</span></span>

[<span data-ttu-id="059a0-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="059a0-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="059a0-145">제거-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="059a0-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="059a0-146">업데이트-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="059a0-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


