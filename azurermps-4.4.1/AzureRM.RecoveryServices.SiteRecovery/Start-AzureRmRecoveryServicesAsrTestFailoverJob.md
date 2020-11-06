---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533904"
---
# <span data-ttu-id="6e72d-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6e72d-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="6e72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e72d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e72d-103">테스트 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e72d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e72d-104">SYNTAX</span></span>

### <span data-ttu-id="6e72d-105">ByRPIObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e72d-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e72d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6e72d-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e72d-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6e72d-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e72d-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e72d-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e72d-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6e72d-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e72d-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e72d-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e72d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="6e72d-111">DESCRIPTION</span></span>
<span data-ttu-id="6e72d-112">**AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획의 장애 조치 테스트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="6e72d-113">Get-AzureRmRecoveryServicesAsrJob cmdlet을 사용 하 여 작업 성공 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="6e72d-114">예제의</span><span class="sxs-lookup"><span data-stu-id="6e72d-114">EXAMPLES</span></span>

### <span data-ttu-id="6e72d-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e72d-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="6e72d-116">복구 계획에 대해 지정 된 매개 변수를 사용 하 여 테스트 장애 조치 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6e72d-117">변수</span><span class="sxs-lookup"><span data-stu-id="6e72d-117">PARAMETERS</span></span>

### <span data-ttu-id="6e72d-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e72d-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="6e72d-119">가상 컴퓨터를 통해 테스트 장애를 연결 하는 Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-120">-Data<c13> Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="6e72d-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6e72d-121">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-121">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-122">-Data<c13> Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="6e72d-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6e72d-123">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-123">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-124">방향</span><span class="sxs-lookup"><span data-stu-id="6e72d-124">-Direction</span></span>
<span data-ttu-id="6e72d-125">장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-125">Specifies the failover direction.</span></span>
<span data-ttu-id="6e72d-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e72d-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6e72d-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="6e72d-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6e72d-128">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e72d-129">-RecoveryPlan</span></span>
<span data-ttu-id="6e72d-130">ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e72d-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6e72d-132">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="6e72d-133">-VMNetwork</span></span>
<span data-ttu-id="6e72d-134">테스트 장애 조치 (failover) 가상 컴퓨터를 연결할 사이트 복구 가상 컴퓨터 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e72d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6e72d-135">-Confirm</span></span>
<span data-ttu-id="6e72d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e72d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e72d-137">-WhatIf</span></span>
<span data-ttu-id="6e72d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e72d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e72d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e72d-140">CommonParameters</span></span>
<span data-ttu-id="6e72d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e72d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e72d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e72d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e72d-143">입력</span><span class="sxs-lookup"><span data-stu-id="6e72d-143">INPUTS</span></span>

### <span data-ttu-id="6e72d-144">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="6e72d-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="6e72d-145">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6e72d-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6e72d-146">출력</span><span class="sxs-lookup"><span data-stu-id="6e72d-146">OUTPUTS</span></span>

### <span data-ttu-id="6e72d-147">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="6e72d-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6e72d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6e72d-148">NOTES</span></span>

## <span data-ttu-id="6e72d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e72d-149">RELATED LINKS</span></span>

[<span data-ttu-id="6e72d-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6e72d-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
