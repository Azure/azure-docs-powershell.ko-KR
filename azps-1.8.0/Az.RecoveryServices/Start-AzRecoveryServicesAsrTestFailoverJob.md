---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: a05467b19aaf69bccdca64c8e17b894941f3ac6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699590"
---
# <span data-ttu-id="11fe8-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="11fe8-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="11fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="11fe8-103">테스트 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="11fe8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11fe8-104">SYNTAX</span></span>

### <span data-ttu-id="11fe8-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="11fe8-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fe8-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="11fe8-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fe8-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="11fe8-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fe8-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="11fe8-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fe8-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="11fe8-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11fe8-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="11fe8-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11fe8-111">설명은</span><span class="sxs-lookup"><span data-stu-id="11fe8-111">DESCRIPTION</span></span>
<span data-ttu-id="11fe8-112">**AzRecoveryServicesAsrTestFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획의 장애 조치 테스트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="11fe8-113">Get-AzRecoveryServicesAsrJob cmdlet을 사용 하 여 작업 성공 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="11fe8-114">예제의</span><span class="sxs-lookup"><span data-stu-id="11fe8-114">EXAMPLES</span></span>

### <span data-ttu-id="11fe8-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="11fe8-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="11fe8-116">복구 계획에 대해 지정 된 매개 변수를 사용 하 여 테스트 장애 조치 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="11fe8-117">변수</span><span class="sxs-lookup"><span data-stu-id="11fe8-117">PARAMETERS</span></span>

### <span data-ttu-id="11fe8-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="11fe8-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="11fe8-119">{{Fill AzureVMNetworkId Description}}</span><span class="sxs-lookup"><span data-stu-id="11fe8-119">{{Fill AzureVMNetworkId Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="11fe8-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="11fe8-121">새 클라우드 서비스를 만들지 아니면 VM에 대해 구성 된 복구 클라우드 서비스를 테스트 장애 조치에 사용 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-122">-Data<c13> Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="11fe8-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="11fe8-123">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="11fe8-124">-Data<c13> Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="11fe8-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="11fe8-125">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="11fe8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fe8-126">-DefaultProfile</span></span>
<span data-ttu-id="11fe8-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="11fe8-128">방향</span><span class="sxs-lookup"><span data-stu-id="11fe8-128">-Direction</span></span>
<span data-ttu-id="11fe8-129">장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-129">Specifies the failover direction.</span></span>
<span data-ttu-id="11fe8-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11fe8-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="11fe8-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="11fe8-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="11fe8-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="11fe8-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="11fe8-133">-RecoveryPlan</span></span>
<span data-ttu-id="11fe8-134">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="11fe8-135">-RecoveryPoint</span></span>
<span data-ttu-id="11fe8-136">보호 된 컴퓨터의 장애 조치를 테스트 하는 사용자 지정 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="11fe8-137">-RecoveryTag</span></span>
<span data-ttu-id="11fe8-138">장애 조치를 테스트할 복구 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="11fe8-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="11fe8-140">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="11fe8-141">-VMNetwork</span></span>
<span data-ttu-id="11fe8-142">테스트 장애 조치 (failover) 가상 컴퓨터를 연결할 사이트 복구 가상 컴퓨터 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe8-143">-확인</span><span class="sxs-lookup"><span data-stu-id="11fe8-143">-Confirm</span></span>
<span data-ttu-id="11fe8-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11fe8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11fe8-145">-WhatIf</span></span>
<span data-ttu-id="11fe8-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11fe8-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11fe8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fe8-148">CommonParameters</span></span>
<span data-ttu-id="11fe8-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11fe8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fe8-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11fe8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fe8-151">입력</span><span class="sxs-lookup"><span data-stu-id="11fe8-151">INPUTS</span></span>

### <span data-ttu-id="11fe8-152">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="11fe8-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="11fe8-153">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="11fe8-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="11fe8-154">출력</span><span class="sxs-lookup"><span data-stu-id="11fe8-154">OUTPUTS</span></span>

### <span data-ttu-id="11fe8-155">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="11fe8-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="11fe8-156">상속자</span><span class="sxs-lookup"><span data-stu-id="11fe8-156">NOTES</span></span>

## <span data-ttu-id="11fe8-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11fe8-157">RELATED LINKS</span></span>

[<span data-ttu-id="11fe8-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="11fe8-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
