---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530655"
---
# <span data-ttu-id="86370-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="86370-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="86370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86370-102">SYNOPSIS</span></span>
<span data-ttu-id="86370-103">사이트 복구 계획 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86370-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86370-104">SYNTAX</span></span>

### <span data-ttu-id="86370-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="86370-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86370-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="86370-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86370-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="86370-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86370-108">설명은</span><span class="sxs-lookup"><span data-stu-id="86370-108">DESCRIPTION</span></span>
<span data-ttu-id="86370-109">**AzureRmSiteRecoveryPlannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획에 대해 계획 된 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="86370-110">Get-AzureRmSiteRecoveryJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86370-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="86370-111">예제의</span><span class="sxs-lookup"><span data-stu-id="86370-111">EXAMPLES</span></span>

## <span data-ttu-id="86370-112">변수</span><span class="sxs-lookup"><span data-stu-id="86370-112">PARAMETERS</span></span>

### <span data-ttu-id="86370-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="86370-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="86370-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86370-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86370-115">'</span><span class="sxs-lookup"><span data-stu-id="86370-115">Yes</span></span>
- <span data-ttu-id="86370-116">아니요</span><span class="sxs-lookup"><span data-stu-id="86370-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-117">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="86370-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="86370-118">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="86370-119">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="86370-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="86370-120">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="86370-121">방향</span><span class="sxs-lookup"><span data-stu-id="86370-121">-Direction</span></span>
<span data-ttu-id="86370-122">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="86370-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86370-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86370-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="86370-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="86370-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="86370-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="86370-126">-최적화</span><span class="sxs-lookup"><span data-stu-id="86370-126">-Optimize</span></span>
<span data-ttu-id="86370-127">최적화 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="86370-128">이 매개 변수는 실제 데이터 동기화가 필요한 Azure 사이트에서 온-프레미스 사이트로 장애 조치를 수행할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86370-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="86370-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86370-129">Valid values are:</span></span>

- <span data-ttu-id="86370-130">ForDowntime 중지 시간</span><span class="sxs-lookup"><span data-stu-id="86370-130">ForDowntime</span></span>
- <span data-ttu-id="86370-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="86370-131">ForSynchronization</span></span>

<span data-ttu-id="86370-132">**Fordowntime** 지정 되 면 가동 중지 시간을 최소화 하기 위해 장애 조치 전에 데이터가 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86370-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="86370-133">동기화는 가상 컴퓨터를 종료 하지 않고 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86370-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="86370-134">동기화가 완료 되 면 작업이 일시 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86370-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="86370-135">작업을 다시 시작 하 여 가상 컴퓨터를 종료 하는 추가 동기화 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="86370-136">**Forsynchronization** 이 지정 된 경우 데이터 동기화가 최소화 될 때만 데이터가 장애 조치 중에 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86370-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="86370-137">이 설정을 사용 하도록 설정 하면 가상 컴퓨터가 즉시 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86370-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="86370-138">장애 조치 작업을 완료 하기 위해 종료 후 동기화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86370-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="86370-139">-ProtectionEntity</span></span>
<span data-ttu-id="86370-140">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86370-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86370-141">-RecoveryPlan</span></span>
<span data-ttu-id="86370-142">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86370-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="86370-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86370-144">-서버</span><span class="sxs-lookup"><span data-stu-id="86370-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-145">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="86370-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86370-146">-DefaultProfile</span></span>
<span data-ttu-id="86370-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86370-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86370-148">CommonParameters</span></span>
<span data-ttu-id="86370-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86370-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86370-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86370-151">입력</span><span class="sxs-lookup"><span data-stu-id="86370-151">INPUTS</span></span>

### <span data-ttu-id="86370-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="86370-152">ASRProtectionEntity</span></span>
<span data-ttu-id="86370-153">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="86370-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="86370-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="86370-155">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="86370-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="86370-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="86370-157">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86370-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="86370-158">출력</span><span class="sxs-lookup"><span data-stu-id="86370-158">OUTPUTS</span></span>

### <span data-ttu-id="86370-159">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="86370-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="86370-160">상속자</span><span class="sxs-lookup"><span data-stu-id="86370-160">NOTES</span></span>

## <span data-ttu-id="86370-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86370-161">RELATED LINKS</span></span>

