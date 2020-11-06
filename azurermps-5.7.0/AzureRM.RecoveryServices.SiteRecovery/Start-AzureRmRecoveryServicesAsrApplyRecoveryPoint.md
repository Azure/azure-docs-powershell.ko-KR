---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525008"
---
# <span data-ttu-id="a045d-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a045d-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="a045d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a045d-102">SYNOPSIS</span></span>
<span data-ttu-id="a045d-103">장애 조치 (failover) 작업을 수행 하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a045d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a045d-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a045d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a045d-105">DESCRIPTION</span></span>
<span data-ttu-id="a045d-106">**AzureRmRecoveryServicesAsrApplyRecoveryPoint** 는 장애 조치 (failover) 작업을 커밋할 때까지 보호 되는 항목이 실패 한 경우 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="a045d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a045d-107">EXAMPLES</span></span>

### <span data-ttu-id="a045d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a045d-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="a045d-109">복제 보호 항목에 지정 된 복구 지점을 적용 하기 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a045d-110">변수</span><span class="sxs-lookup"><span data-stu-id="a045d-110">PARAMETERS</span></span>

### <span data-ttu-id="a045d-111">-확인</span><span class="sxs-lookup"><span data-stu-id="a045d-111">-Confirm</span></span>
<span data-ttu-id="a045d-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a045d-113">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="a045d-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a045d-114">데이터 암호화를 사용 하는 경우 기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="a045d-115">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="a045d-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a045d-116">데이터 암호화를 사용 하는 경우 보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="a045d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a045d-117">-DefaultProfile</span></span>
<span data-ttu-id="a045d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="a045d-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a045d-119">-RecoveryPoint</span></span>
<span data-ttu-id="a045d-120">적용 되는 복구 시점에 해당 하는 복구 시점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a045d-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a045d-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a045d-122">ASR 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-122">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a045d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a045d-123">-WhatIf</span></span>
<span data-ttu-id="a045d-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a045d-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a045d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a045d-126">CommonParameters</span></span>
<span data-ttu-id="a045d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a045d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a045d-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a045d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a045d-129">입력</span><span class="sxs-lookup"><span data-stu-id="a045d-129">INPUTS</span></span>

### <span data-ttu-id="a045d-130">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="a045d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a045d-131">출력</span><span class="sxs-lookup"><span data-stu-id="a045d-131">OUTPUTS</span></span>

### <span data-ttu-id="a045d-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="a045d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a045d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a045d-133">NOTES</span></span>

## <span data-ttu-id="a045d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a045d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a045d-135">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a045d-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
