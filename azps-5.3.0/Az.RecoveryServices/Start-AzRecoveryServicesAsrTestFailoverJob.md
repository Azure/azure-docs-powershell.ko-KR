---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378351"
---
# <span data-ttu-id="7cd91-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7cd91-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="7cd91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd91-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd91-103">테스트 장애 조치(failover) 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="7cd91-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cd91-104">SYNTAX</span></span>

### <span data-ttu-id="7cd91-105">ByRPIObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="7cd91-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd91-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7cd91-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd91-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7cd91-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd91-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7cd91-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd91-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="7cd91-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd91-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7cd91-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cd91-111">설명</span><span class="sxs-lookup"><span data-stu-id="7cd91-111">DESCRIPTION</span></span>
<span data-ttu-id="7cd91-112">**Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet은 Azure Site Recovery 복제 보호된 항목 또는 복구 계획의 테스트 장애 조치(failover)를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="7cd91-113">Get-AzRecoveryServicesAsrJob cmdlet을 사용하여 작업이 성공하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="7cd91-114">예제</span><span class="sxs-lookup"><span data-stu-id="7cd91-114">EXAMPLES</span></span>

### <span data-ttu-id="7cd91-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cd91-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="7cd91-116">지정된 매개 변수를 사용하여 복구 계획에 대한 테스트 장애 조치(failover) 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7cd91-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="7cd91-117">Example 2</span></span>

<span data-ttu-id="7cd91-118">테스트 장애 조치(failover) 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-118">Starts a test failover operation.</span></span> <span data-ttu-id="7cd91-119">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="7cd91-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="7cd91-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cd91-120">PARAMETERS</span></span>

### <span data-ttu-id="7cd91-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7cd91-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="7cd91-122">장애 조치(failover) 후 복구 VM에 대한 Azure VM 네트워크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="7cd91-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="7cd91-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="7cd91-124">새 클라우드 서비스를 만들어야 하는지 또는 VM에 대해 구성된 복구 클라우드 서비스를 테스트 장애 조치(failover)에 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="7cd91-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7cd91-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="7cd91-126">기본 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="7cd91-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7cd91-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="7cd91-128">보조 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="7cd91-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd91-129">-DefaultProfile</span></span>
<span data-ttu-id="7cd91-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7cd91-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="7cd91-131">-Direction</span></span>
<span data-ttu-id="7cd91-132">장애 조치 방향을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-132">Specifies the failover direction.</span></span>
<span data-ttu-id="7cd91-133">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="7cd91-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7cd91-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7cd91-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="7cd91-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7cd91-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="7cd91-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7cd91-136">-RecoveryPlan</span></span>
<span data-ttu-id="7cd91-137">ASR 복구 계획 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="7cd91-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7cd91-138">-RecoveryPoint</span></span>
<span data-ttu-id="7cd91-139">보호된 머신을 테스트할 사용자 지정 복구 지점을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="7cd91-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="7cd91-140">-RecoveryTag</span></span>
<span data-ttu-id="7cd91-141">장애 조치(failover)를 테스트할 복구 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="7cd91-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7cd91-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7cd91-143">ASR 복제 보호 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="7cd91-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="7cd91-144">-VMNetwork</span></span>
<span data-ttu-id="7cd91-145">테스트 장애 조치(failover) 가상 머신을 연결할 Site Recovery 가상 머신 네트워크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="7cd91-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd91-146">-Confirm</span></span>
<span data-ttu-id="7cd91-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd91-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd91-148">-WhatIf</span></span>
<span data-ttu-id="7cd91-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7cd91-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cd91-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd91-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd91-151">CommonParameters</span></span>
<span data-ttu-id="7cd91-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd91-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd91-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7cd91-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd91-154">입력</span><span class="sxs-lookup"><span data-stu-id="7cd91-154">INPUTS</span></span>

### <span data-ttu-id="7cd91-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7cd91-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="7cd91-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7cd91-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7cd91-157">출력</span><span class="sxs-lookup"><span data-stu-id="7cd91-157">OUTPUTS</span></span>

### <span data-ttu-id="7cd91-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7cd91-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7cd91-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cd91-159">NOTES</span></span>

## <span data-ttu-id="7cd91-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cd91-160">RELATED LINKS</span></span>

[<span data-ttu-id="7cd91-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7cd91-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
