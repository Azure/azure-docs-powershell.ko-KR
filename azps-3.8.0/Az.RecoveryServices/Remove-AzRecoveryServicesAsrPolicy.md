---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042641"
---
# <span data-ttu-id="91e76-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e76-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="91e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e76-102">SYNOPSIS</span></span>
<span data-ttu-id="91e76-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 복제 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="91e76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91e76-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91e76-105">DESCRIPTION</span></span>
<span data-ttu-id="91e76-106">**AzRecoveryServicesAsrPolicy** Cmdlet이 복구 서비스 자격 증명 모음에서 지정 된 복제 정책을 삭제 했습니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="91e76-107">예제의</span><span class="sxs-lookup"><span data-stu-id="91e76-107">EXAMPLES</span></span>

### <span data-ttu-id="91e76-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="91e76-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="91e76-109">지정 된 복제 정책의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="91e76-110">변수</span><span class="sxs-lookup"><span data-stu-id="91e76-110">PARAMETERS</span></span>

### <span data-ttu-id="91e76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e76-111">-DefaultProfile</span></span>
<span data-ttu-id="91e76-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="91e76-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91e76-113">-InputObject</span></span>
<span data-ttu-id="91e76-114">Cmdlet에 대 한 입력 개체: 삭제할 복제 정책에 해당 하는 ASR 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e76-115">-확인</span><span class="sxs-lookup"><span data-stu-id="91e76-115">-Confirm</span></span>
<span data-ttu-id="91e76-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e76-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e76-117">-WhatIf</span></span>
<span data-ttu-id="91e76-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91e76-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e76-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e76-120">CommonParameters</span></span>
<span data-ttu-id="91e76-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91e76-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e76-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91e76-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e76-123">입력</span><span class="sxs-lookup"><span data-stu-id="91e76-123">INPUTS</span></span>

### <span data-ttu-id="91e76-124">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="91e76-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="91e76-125">출력</span><span class="sxs-lookup"><span data-stu-id="91e76-125">OUTPUTS</span></span>

### <span data-ttu-id="91e76-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="91e76-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91e76-127">상속자</span><span class="sxs-lookup"><span data-stu-id="91e76-127">NOTES</span></span>

## <span data-ttu-id="91e76-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91e76-128">RELATED LINKS</span></span>

[<span data-ttu-id="91e76-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e76-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="91e76-130">새로운 AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e76-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
