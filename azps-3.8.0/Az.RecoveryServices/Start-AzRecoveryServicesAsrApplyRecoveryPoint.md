---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043515"
---
# <span data-ttu-id="5b112-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5b112-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="5b112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b112-102">SYNOPSIS</span></span>
<span data-ttu-id="5b112-103">장애 조치 (failover) 작업을 커밋하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="5b112-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b112-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b112-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b112-105">DESCRIPTION</span></span>
<span data-ttu-id="5b112-106">**AzRecoveryServicesAsrApplyRecoveryPoint** 는 장애 조치 (failover) 작업을 커밋할 때까지 보호 되는 항목이 실패 한 경우 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="5b112-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b112-107">EXAMPLES</span></span>

### <span data-ttu-id="5b112-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b112-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="5b112-109">복제 보호 항목에 지정 된 복구 지점을 적용 하기 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5b112-110">변수</span><span class="sxs-lookup"><span data-stu-id="5b112-110">PARAMETERS</span></span>

### <span data-ttu-id="5b112-111">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="5b112-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="5b112-112">데이터 암호화를 사용 하는 경우 기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="5b112-113">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="5b112-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="5b112-114">데이터 암호화를 사용 하는 경우 보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="5b112-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b112-115">-DefaultProfile</span></span>
<span data-ttu-id="5b112-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5b112-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5b112-117">-RecoveryPoint</span></span>
<span data-ttu-id="5b112-118">적용 되는 복구 시점에 해당 하는 복구 시점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b112-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5b112-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5b112-120">ASR 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b112-121">-확인</span><span class="sxs-lookup"><span data-stu-id="5b112-121">-Confirm</span></span>
<span data-ttu-id="5b112-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b112-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b112-123">-WhatIf</span></span>
<span data-ttu-id="5b112-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b112-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b112-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b112-126">CommonParameters</span></span>
<span data-ttu-id="5b112-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b112-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b112-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b112-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b112-129">입력</span><span class="sxs-lookup"><span data-stu-id="5b112-129">INPUTS</span></span>

### <span data-ttu-id="5b112-130">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="5b112-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5b112-131">출력</span><span class="sxs-lookup"><span data-stu-id="5b112-131">OUTPUTS</span></span>

### <span data-ttu-id="5b112-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="5b112-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5b112-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5b112-133">NOTES</span></span>

## <span data-ttu-id="5b112-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b112-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b112-135">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b112-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
