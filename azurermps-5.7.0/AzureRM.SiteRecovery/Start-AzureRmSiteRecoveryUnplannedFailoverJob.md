---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524892"
---
# <span data-ttu-id="84147-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="84147-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="84147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84147-102">SYNOPSIS</span></span>
<span data-ttu-id="84147-103">사이트 복구 보호 엔터티 또는 복구 계획에 대해 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84147-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84147-104">SYNTAX</span></span>

### <span data-ttu-id="84147-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="84147-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84147-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="84147-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84147-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="84147-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84147-108">설명은</span><span class="sxs-lookup"><span data-stu-id="84147-108">DESCRIPTION</span></span>
<span data-ttu-id="84147-109">**AzureRmSiteRecoveryUnplannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획의 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="84147-110">Get-AzureRmSiteRecoveryJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84147-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="84147-111">예제의</span><span class="sxs-lookup"><span data-stu-id="84147-111">EXAMPLES</span></span>

## <span data-ttu-id="84147-112">변수</span><span class="sxs-lookup"><span data-stu-id="84147-112">PARAMETERS</span></span>

### <span data-ttu-id="84147-113">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="84147-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="84147-114">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="84147-115">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="84147-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="84147-116">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="84147-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84147-117">-DefaultProfile</span></span>
<span data-ttu-id="84147-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84147-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84147-119">방향</span><span class="sxs-lookup"><span data-stu-id="84147-119">-Direction</span></span>
<span data-ttu-id="84147-120">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="84147-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84147-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="84147-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="84147-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="84147-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="84147-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="84147-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="84147-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="84147-125">작업이 원본 사이트 작업을 수행할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84147-125">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84147-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="84147-126">-ProtectionEntity</span></span>
<span data-ttu-id="84147-127">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-127">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="84147-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84147-128">-RecoveryPlan</span></span>
<span data-ttu-id="84147-129">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-129">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="84147-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84147-130">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="84147-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84147-131">CommonParameters</span></span>
<span data-ttu-id="84147-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84147-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84147-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84147-134">입력</span><span class="sxs-lookup"><span data-stu-id="84147-134">INPUTS</span></span>

### <span data-ttu-id="84147-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="84147-135">ASRProtectionEntity</span></span>
<span data-ttu-id="84147-136">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="84147-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84147-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="84147-138">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="84147-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84147-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="84147-140">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84147-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="84147-141">출력</span><span class="sxs-lookup"><span data-stu-id="84147-141">OUTPUTS</span></span>

### <span data-ttu-id="84147-142">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="84147-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84147-143">상속자</span><span class="sxs-lookup"><span data-stu-id="84147-143">NOTES</span></span>

## <span data-ttu-id="84147-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84147-144">RELATED LINKS</span></span>

[<span data-ttu-id="84147-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="84147-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


