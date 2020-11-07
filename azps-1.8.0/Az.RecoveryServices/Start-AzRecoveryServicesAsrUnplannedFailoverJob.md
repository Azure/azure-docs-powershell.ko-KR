---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: fa02e7e4b6d98f22c386616a8ebfedad88ba0b40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699588"
---
# <span data-ttu-id="0001c-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0001c-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="0001c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0001c-102">SYNOPSIS</span></span>
<span data-ttu-id="0001c-103">계획 되지 않은 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-103">Starts a unplanned failover operation.</span></span>

## <span data-ttu-id="0001c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0001c-104">SYNTAX</span></span>

### <span data-ttu-id="0001c-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="0001c-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0001c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0001c-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0001c-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0001c-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0001c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0001c-108">DESCRIPTION</span></span>
<span data-ttu-id="0001c-109">**AzRecoveryServicesAsrTestFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획의 장애 조치 테스트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-109">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0001c-110">Get-AzRecoveryServicesAsrJob cmdlet을 사용 하 여 작업 성공 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0001c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0001c-111">EXAMPLES</span></span>

### <span data-ttu-id="0001c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0001c-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="0001c-113">복구 계획에 대해 지정 된 매개 변수를 사용 하 여 테스트 장애 조치 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0001c-114">변수</span><span class="sxs-lookup"><span data-stu-id="0001c-114">PARAMETERS</span></span>

### <span data-ttu-id="0001c-115">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="0001c-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0001c-116">보호 된 항목의 장애 조치 (failover)에 대 한 데이터 암호화 기본 인증서 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-117">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="0001c-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0001c-118">보호 된 항목의 장애 조치 (failover)에 대 한 데이터 암호화 보조 인증서 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0001c-119">-DefaultProfile</span></span>
<span data-ttu-id="0001c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0001c-121">방향</span><span class="sxs-lookup"><span data-stu-id="0001c-121">-Direction</span></span>
<span data-ttu-id="0001c-122">장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-122">Specifies the failover direction.</span></span>
<span data-ttu-id="0001c-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0001c-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0001c-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="0001c-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0001c-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="0001c-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="0001c-127">계획 되지 않은 장애 조치를 시작 하기 전에 원본 측에서 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0001c-128">-RecoveryPlan</span></span>
<span data-ttu-id="0001c-129">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-129">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0001c-130">-RecoveryPoint</span></span>
<span data-ttu-id="0001c-131">보호 된 컴퓨터를 장애 조치 (failover) 할 사용자 지정 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0001c-132">-RecoveryTag</span></span>
<span data-ttu-id="0001c-133">장애 조치 (failover) 할 복구 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0001c-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0001c-135">Azure site recovery 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0001c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="0001c-136">-Confirm</span></span>
<span data-ttu-id="0001c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0001c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0001c-138">-WhatIf</span></span>
<span data-ttu-id="0001c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0001c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0001c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0001c-141">CommonParameters</span></span>
<span data-ttu-id="0001c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0001c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0001c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0001c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0001c-144">입력</span><span class="sxs-lookup"><span data-stu-id="0001c-144">INPUTS</span></span>

### <span data-ttu-id="0001c-145">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="0001c-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="0001c-146">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="0001c-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0001c-147">출력</span><span class="sxs-lookup"><span data-stu-id="0001c-147">OUTPUTS</span></span>

### <span data-ttu-id="0001c-148">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="0001c-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0001c-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0001c-149">NOTES</span></span>

## <span data-ttu-id="0001c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0001c-150">RELATED LINKS</span></span>

[<span data-ttu-id="0001c-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0001c-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
