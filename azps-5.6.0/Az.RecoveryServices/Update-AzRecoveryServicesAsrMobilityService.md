---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 5c5c9509c7ae242f98c8474a2ab87635f94dd62d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970368"
---
# <span data-ttu-id="c328b-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="c328b-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="c328b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c328b-102">SYNOPSIS</span></span>
<span data-ttu-id="c328b-103">모바일 서비스 에이전트 업데이트를 보호된 컴퓨터로 푸시합니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="c328b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c328b-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c328b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c328b-105">DESCRIPTION</span></span>
<span data-ttu-id="c328b-106">**Update-AzRecoveryServicesAsrMobilityService** cmdlet은 모바일 서비스 에이전트 업데이트를 보호된 컴퓨터로 푸시하려고 시도합니다(업데이트를 사용할 수 있는 경우).</span><span class="sxs-lookup"><span data-stu-id="c328b-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="c328b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c328b-107">EXAMPLES</span></span>

### <span data-ttu-id="c328b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c328b-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="c328b-109">복제 보호 항목의 모바일 서비스 에이전트 업데이트 추적 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="c328b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c328b-110">PARAMETERS</span></span>

### <span data-ttu-id="c328b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c328b-111">-Account</span></span>
<span data-ttu-id="c328b-112">업데이트를 푸시하는 데 사용할 계정 ID로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="c328b-113">업데이트되는 머신에 해당하는 ASR 패브릭의 계정으로 실행 목록에서 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c328b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c328b-114">-DefaultProfile</span></span>
<span data-ttu-id="c328b-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c328b-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c328b-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c328b-117">업데이트할 Azure Site Recovery 복제로 보호된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="c328b-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c328b-118">-Confirm</span></span>
<span data-ttu-id="c328b-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c328b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c328b-120">-WhatIf</span></span>
<span data-ttu-id="c328b-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c328b-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c328b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c328b-123">CommonParameters</span></span>
<span data-ttu-id="c328b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c328b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c328b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c328b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c328b-126">입력</span><span class="sxs-lookup"><span data-stu-id="c328b-126">INPUTS</span></span>

### <span data-ttu-id="c328b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c328b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c328b-128">출력</span><span class="sxs-lookup"><span data-stu-id="c328b-128">OUTPUTS</span></span>

### <span data-ttu-id="c328b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c328b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c328b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c328b-130">NOTES</span></span>

## <span data-ttu-id="c328b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c328b-131">RELATED LINKS</span></span>
