---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703955"
---
# <span data-ttu-id="02532-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="02532-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="02532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02532-102">SYNOPSIS</span></span>
<span data-ttu-id="02532-103">사이트 복구 계획 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02532-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02532-104">SYNTAX</span></span>

### <span data-ttu-id="02532-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="02532-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02532-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="02532-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02532-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="02532-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02532-108">설명은</span><span class="sxs-lookup"><span data-stu-id="02532-108">DESCRIPTION</span></span>
<span data-ttu-id="02532-109">**AzureRmSiteRecoveryPlannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획에 대해 계획 된 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="02532-110">Get-AzureRmSiteRecoveryJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02532-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="02532-111">예제의</span><span class="sxs-lookup"><span data-stu-id="02532-111">EXAMPLES</span></span>

## <span data-ttu-id="02532-112">변수</span><span class="sxs-lookup"><span data-stu-id="02532-112">PARAMETERS</span></span>

### <span data-ttu-id="02532-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="02532-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="02532-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="02532-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02532-115">'</span><span class="sxs-lookup"><span data-stu-id="02532-115">Yes</span></span>
- <span data-ttu-id="02532-116">아니요</span><span class="sxs-lookup"><span data-stu-id="02532-116">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02532-117">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="02532-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="02532-118">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="02532-119">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="02532-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="02532-120">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="02532-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02532-121">-DefaultProfile</span></span>
<span data-ttu-id="02532-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02532-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02532-123">방향</span><span class="sxs-lookup"><span data-stu-id="02532-123">-Direction</span></span>
<span data-ttu-id="02532-124">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="02532-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="02532-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02532-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="02532-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="02532-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="02532-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="02532-128">-최적화</span><span class="sxs-lookup"><span data-stu-id="02532-128">-Optimize</span></span>
<span data-ttu-id="02532-129">최적화 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="02532-130">이 매개 변수는 실제 데이터 동기화가 필요한 Azure 사이트에서 온-프레미스 사이트로 장애 조치를 수행할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02532-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="02532-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="02532-131">Valid values are:</span></span>

- <span data-ttu-id="02532-132">ForDowntime 중지 시간</span><span class="sxs-lookup"><span data-stu-id="02532-132">ForDowntime</span></span>
- <span data-ttu-id="02532-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="02532-133">ForSynchronization</span></span>

<span data-ttu-id="02532-134">**Fordowntime** 지정 되 면 가동 중지 시간을 최소화 하기 위해 장애 조치 전에 데이터가 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="02532-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="02532-135">동기화는 가상 컴퓨터를 종료 하지 않고 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02532-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="02532-136">동기화가 완료 되 면 작업이 일시 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02532-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="02532-137">작업을 다시 시작 하 여 가상 컴퓨터를 종료 하는 추가 동기화 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="02532-138">**Forsynchronization** 이 지정 된 경우 데이터 동기화가 최소화 될 때만 데이터가 장애 조치 중에 동기화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="02532-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="02532-139">이 설정을 사용 하도록 설정 하면 가상 컴퓨터가 즉시 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02532-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="02532-140">장애 조치 작업을 완료 하기 위해 종료 후 동기화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02532-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02532-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="02532-141">-ProtectionEntity</span></span>
<span data-ttu-id="02532-142">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02532-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02532-143">-RecoveryPlan</span></span>
<span data-ttu-id="02532-144">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-144">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02532-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02532-145">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02532-146">-서버</span><span class="sxs-lookup"><span data-stu-id="02532-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02532-147">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="02532-147">-ServicesProvider</span></span>
```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02532-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02532-148">CommonParameters</span></span>
<span data-ttu-id="02532-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02532-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02532-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02532-151">입력</span><span class="sxs-lookup"><span data-stu-id="02532-151">INPUTS</span></span>

### <span data-ttu-id="02532-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="02532-152">ASRProtectionEntity</span></span>
<span data-ttu-id="02532-153">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="02532-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="02532-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="02532-155">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="02532-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02532-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="02532-157">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02532-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="02532-158">출력</span><span class="sxs-lookup"><span data-stu-id="02532-158">OUTPUTS</span></span>

### <span data-ttu-id="02532-159">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="02532-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02532-160">상속자</span><span class="sxs-lookup"><span data-stu-id="02532-160">NOTES</span></span>

## <span data-ttu-id="02532-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02532-161">RELATED LINKS</span></span>

