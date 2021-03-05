---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 748278cd6096a8ab67538df77aa3b81cc54d3ace
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960240"
---
# <span data-ttu-id="753f6-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="753f6-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="753f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753f6-102">SYNOPSIS</span></span>
<span data-ttu-id="753f6-103">장애 조치(failover) 작업을 커밋하기 전에 장애 조치(failover) 보호된 항목에 대한 복구 지점을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="753f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="753f6-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="753f6-105">설명</span><span class="sxs-lookup"><span data-stu-id="753f6-105">DESCRIPTION</span></span>
<span data-ttu-id="753f6-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint는** 장애 조치(failover) 작업을 커밋하기 전에 보호되지 못한 보호된 항목에 대한 복구 지점을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="753f6-107">예제</span><span class="sxs-lookup"><span data-stu-id="753f6-107">EXAMPLES</span></span>

### <span data-ttu-id="753f6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="753f6-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="753f6-109">지정된 복구 지점을 복제 보호 항목에 적용하기 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="753f6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="753f6-110">PARAMETERS</span></span>

### <span data-ttu-id="753f6-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="753f6-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="753f6-112">데이터 암호화를 사용하는 경우 기본 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="753f6-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="753f6-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="753f6-114">데이터 암호화가 사용되는 경우 보조 인증서 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="753f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753f6-115">-DefaultProfile</span></span>
<span data-ttu-id="753f6-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="753f6-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="753f6-117">-RecoveryPoint</span></span>
<span data-ttu-id="753f6-118">적용할 복구 지점에 해당하는 복구 지점 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="753f6-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="753f6-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="753f6-120">ASR 복제로 보호된 항목 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="753f6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="753f6-121">-Confirm</span></span>
<span data-ttu-id="753f6-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="753f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="753f6-123">-WhatIf</span></span>
<span data-ttu-id="753f6-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="753f6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="753f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753f6-126">CommonParameters</span></span>
<span data-ttu-id="753f6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="753f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753f6-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="753f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753f6-129">입력</span><span class="sxs-lookup"><span data-stu-id="753f6-129">INPUTS</span></span>

### <span data-ttu-id="753f6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="753f6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="753f6-131">출력</span><span class="sxs-lookup"><span data-stu-id="753f6-131">OUTPUTS</span></span>

### <span data-ttu-id="753f6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="753f6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="753f6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="753f6-133">NOTES</span></span>

## <span data-ttu-id="753f6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="753f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="753f6-135">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="753f6-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
