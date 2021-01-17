---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492433"
---
# <span data-ttu-id="70f99-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="70f99-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="70f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f99-102">SYNOPSIS</span></span>
<span data-ttu-id="70f99-103">Recovery Services 자격 증명 모음에서 지정된 ASR 복제 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="70f99-104">구문</span><span class="sxs-lookup"><span data-stu-id="70f99-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f99-105">설명</span><span class="sxs-lookup"><span data-stu-id="70f99-105">DESCRIPTION</span></span>
<span data-ttu-id="70f99-106">**Remove-AzRecoveryServicesAsrPolicy** cmdlet은 Recovery Services 자격 증명 모음에서 지정된 복제 정책을 삭제했습니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="70f99-107">예제</span><span class="sxs-lookup"><span data-stu-id="70f99-107">EXAMPLES</span></span>

### <span data-ttu-id="70f99-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="70f99-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="70f99-109">지정된 복제 정책의 지우기 시작 및 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="70f99-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70f99-110">PARAMETERS</span></span>

### <span data-ttu-id="70f99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f99-111">-DefaultProfile</span></span>
<span data-ttu-id="70f99-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="70f99-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70f99-113">-InputObject</span></span>
<span data-ttu-id="70f99-114">cmdlet에 대한 입력 개체: 삭제할 복제 정책에 해당하는 ASR 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="70f99-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70f99-115">-Confirm</span></span>
<span data-ttu-id="70f99-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f99-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f99-117">-WhatIf</span></span>
<span data-ttu-id="70f99-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="70f99-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70f99-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f99-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f99-120">CommonParameters</span></span>
<span data-ttu-id="70f99-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70f99-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f99-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70f99-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f99-123">입력</span><span class="sxs-lookup"><span data-stu-id="70f99-123">INPUTS</span></span>

### <span data-ttu-id="70f99-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="70f99-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="70f99-125">출력</span><span class="sxs-lookup"><span data-stu-id="70f99-125">OUTPUTS</span></span>

### <span data-ttu-id="70f99-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="70f99-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70f99-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70f99-127">NOTES</span></span>

## <span data-ttu-id="70f99-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70f99-128">RELATED LINKS</span></span>

[<span data-ttu-id="70f99-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="70f99-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="70f99-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="70f99-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
