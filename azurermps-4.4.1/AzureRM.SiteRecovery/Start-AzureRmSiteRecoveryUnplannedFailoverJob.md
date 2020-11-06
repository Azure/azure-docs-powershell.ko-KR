---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527260"
---
# <span data-ttu-id="56e57-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="56e57-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="56e57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e57-102">SYNOPSIS</span></span>
<span data-ttu-id="56e57-103">사이트 복구 보호 엔터티 또는 복구 계획에 대해 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56e57-104">SYNTAX</span></span>

### <span data-ttu-id="56e57-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="56e57-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56e57-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="56e57-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56e57-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="56e57-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e57-108">설명은</span><span class="sxs-lookup"><span data-stu-id="56e57-108">DESCRIPTION</span></span>
<span data-ttu-id="56e57-109">**AzureRmSiteRecoveryUnplannedFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획의 계획 되지 않은 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="56e57-110">Get-AzureRmSiteRecoveryJob cmdlet을 사용 하 여 작업이 성공 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="56e57-111">예제의</span><span class="sxs-lookup"><span data-stu-id="56e57-111">EXAMPLES</span></span>

## <span data-ttu-id="56e57-112">변수</span><span class="sxs-lookup"><span data-stu-id="56e57-112">PARAMETERS</span></span>

### <span data-ttu-id="56e57-113">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="56e57-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="56e57-114">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="56e57-115">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="56e57-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="56e57-116">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="56e57-117">방향</span><span class="sxs-lookup"><span data-stu-id="56e57-117">-Direction</span></span>
<span data-ttu-id="56e57-118">장애 조치의 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="56e57-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56e57-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="56e57-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="56e57-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="56e57-121">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="56e57-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="56e57-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="56e57-123">작업이 원본 사이트 작업을 수행할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-123">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e57-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e57-124">-ProtectionEntity</span></span>
<span data-ttu-id="56e57-125">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-125">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="56e57-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56e57-126">-RecoveryPlan</span></span>
<span data-ttu-id="56e57-127">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-127">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="56e57-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56e57-128">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="56e57-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e57-129">-DefaultProfile</span></span>
<span data-ttu-id="56e57-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e57-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e57-131">CommonParameters</span></span>
<span data-ttu-id="56e57-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e57-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e57-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e57-134">입력</span><span class="sxs-lookup"><span data-stu-id="56e57-134">INPUTS</span></span>

### <span data-ttu-id="56e57-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e57-135">ASRProtectionEntity</span></span>
<span data-ttu-id="56e57-136">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="56e57-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56e57-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="56e57-138">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="56e57-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56e57-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="56e57-140">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e57-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="56e57-141">출력</span><span class="sxs-lookup"><span data-stu-id="56e57-141">OUTPUTS</span></span>

### <span data-ttu-id="56e57-142">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="56e57-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56e57-143">상속자</span><span class="sxs-lookup"><span data-stu-id="56e57-143">NOTES</span></span>

## <span data-ttu-id="56e57-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56e57-144">RELATED LINKS</span></span>

[<span data-ttu-id="56e57-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="56e57-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


