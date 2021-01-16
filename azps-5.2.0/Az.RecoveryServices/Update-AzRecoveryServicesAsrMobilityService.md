---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358065"
---
# <span data-ttu-id="410c8-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="410c8-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="410c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410c8-102">SYNOPSIS</span></span>
<span data-ttu-id="410c8-103">보호된 머신에 모바일 서비스 에이전트 업데이트를 푸시합니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="410c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="410c8-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410c8-105">설명</span><span class="sxs-lookup"><span data-stu-id="410c8-105">DESCRIPTION</span></span>
<span data-ttu-id="410c8-106">**Update-AzRecoveryServicesAsrMobilityService** cmdlet은 모바일 서비스 에이전트 업데이트를 보호된 컴퓨터로 푸시하려고 합니다(업데이트를 사용할 수 있는 경우).</span><span class="sxs-lookup"><span data-stu-id="410c8-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="410c8-107">예제</span><span class="sxs-lookup"><span data-stu-id="410c8-107">EXAMPLES</span></span>

### <span data-ttu-id="410c8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="410c8-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="410c8-109">복제 보호된 항목의 모바일 서비스 에이전트 업데이트 추적 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="410c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="410c8-110">PARAMETERS</span></span>

### <span data-ttu-id="410c8-111">-Account</span><span class="sxs-lookup"><span data-stu-id="410c8-111">-Account</span></span>
<span data-ttu-id="410c8-112">업데이트를 푸시하는 데 사용할 계정 ID로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="410c8-113">업데이트되는 머신에 해당하는 ASR 패브릭의 실행 계정 목록에서 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="410c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410c8-114">-DefaultProfile</span></span>
<span data-ttu-id="410c8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="410c8-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="410c8-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="410c8-117">업데이트할 Azure Site Recovery 복제 보호된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="410c8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="410c8-118">-Confirm</span></span>
<span data-ttu-id="410c8-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410c8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410c8-120">-WhatIf</span></span>
<span data-ttu-id="410c8-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="410c8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="410c8-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410c8-123">CommonParameters</span></span>
<span data-ttu-id="410c8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="410c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410c8-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="410c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410c8-126">입력</span><span class="sxs-lookup"><span data-stu-id="410c8-126">INPUTS</span></span>

### <span data-ttu-id="410c8-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="410c8-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="410c8-128">출력</span><span class="sxs-lookup"><span data-stu-id="410c8-128">OUTPUTS</span></span>

### <span data-ttu-id="410c8-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="410c8-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="410c8-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="410c8-130">NOTES</span></span>

## <span data-ttu-id="410c8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="410c8-131">RELATED LINKS</span></span>
