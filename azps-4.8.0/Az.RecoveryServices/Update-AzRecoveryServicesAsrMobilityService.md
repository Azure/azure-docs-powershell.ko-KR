---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056075"
---
# <span data-ttu-id="440a7-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="440a7-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="440a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="440a7-102">SYNOPSIS</span></span>
<span data-ttu-id="440a7-103">보호 된 컴퓨터에 모바일 서비스 에이전트 업데이트를 푸시 합니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="440a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="440a7-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="440a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="440a7-105">DESCRIPTION</span></span>
<span data-ttu-id="440a7-106">**업데이트 AzRecoveryServicesAsrMobilityService** cmdlet은 보호 된 컴퓨터에 대 한 모바일 서비스 에이전트 업데이트를 푸시 하려고 합니다 (업데이트를 사용할 수 있는 경우).</span><span class="sxs-lookup"><span data-stu-id="440a7-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="440a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="440a7-107">EXAMPLES</span></span>

### <span data-ttu-id="440a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="440a7-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="440a7-109">복제 보호 항목의 모바일 서비스 에이전트 업데이트를 추적 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="440a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="440a7-110">PARAMETERS</span></span>

### <span data-ttu-id="440a7-111">-계정</span><span class="sxs-lookup"><span data-stu-id="440a7-111">-Account</span></span>
<span data-ttu-id="440a7-112">업데이트를 푸시 하는 데 사용 되는 실행 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="440a7-113">업데이트 하는 컴퓨터에 해당 하는 ASR 패브릭의 실행 계정 목록에서 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="440a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440a7-114">-DefaultProfile</span></span>
<span data-ttu-id="440a7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="440a7-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="440a7-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="440a7-117">업데이트할 Azure Site Recovery 복제 보호 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="440a7-118">-확인</span><span class="sxs-lookup"><span data-stu-id="440a7-118">-Confirm</span></span>
<span data-ttu-id="440a7-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440a7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440a7-120">-WhatIf</span></span>
<span data-ttu-id="440a7-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="440a7-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440a7-123">CommonParameters</span></span>
<span data-ttu-id="440a7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="440a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440a7-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="440a7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440a7-126">입력</span><span class="sxs-lookup"><span data-stu-id="440a7-126">INPUTS</span></span>

### <span data-ttu-id="440a7-127">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="440a7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="440a7-128">출력</span><span class="sxs-lookup"><span data-stu-id="440a7-128">OUTPUTS</span></span>

### <span data-ttu-id="440a7-129">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="440a7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="440a7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="440a7-130">NOTES</span></span>

## <span data-ttu-id="440a7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="440a7-131">RELATED LINKS</span></span>
