---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953275"
---
# <span data-ttu-id="111dc-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="111dc-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="111dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="111dc-102">SYNOPSIS</span></span>
<span data-ttu-id="111dc-103">Recovery Services 자격 증명 모음에서 지정된 ASR 복제 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="111dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="111dc-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="111dc-105">설명</span><span class="sxs-lookup"><span data-stu-id="111dc-105">DESCRIPTION</span></span>
<span data-ttu-id="111dc-106">**Remove-AzRecoveryServicesAsrPolicy** cmdlet은 Recovery Services 자격 증명 모음에서 지정된 복제 정책을 삭제했습니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="111dc-107">예제</span><span class="sxs-lookup"><span data-stu-id="111dc-107">EXAMPLES</span></span>

### <span data-ttu-id="111dc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="111dc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="111dc-109">지정된 복제 정책의 지우기 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="111dc-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="111dc-110">PARAMETERS</span></span>

### <span data-ttu-id="111dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111dc-111">-DefaultProfile</span></span>
<span data-ttu-id="111dc-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="111dc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="111dc-113">-InputObject</span></span>
<span data-ttu-id="111dc-114">cmdlet에 대한 입력 개체: 삭제할 복제 정책에 해당하는 ASR 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="111dc-115">-확인</span><span class="sxs-lookup"><span data-stu-id="111dc-115">-Confirm</span></span>
<span data-ttu-id="111dc-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111dc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111dc-117">-WhatIf</span></span>
<span data-ttu-id="111dc-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="111dc-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111dc-120">CommonParameters</span></span>
<span data-ttu-id="111dc-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="111dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111dc-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="111dc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111dc-123">입력</span><span class="sxs-lookup"><span data-stu-id="111dc-123">INPUTS</span></span>

### <span data-ttu-id="111dc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="111dc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="111dc-125">출력</span><span class="sxs-lookup"><span data-stu-id="111dc-125">OUTPUTS</span></span>

### <span data-ttu-id="111dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="111dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="111dc-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="111dc-127">NOTES</span></span>

## <span data-ttu-id="111dc-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="111dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="111dc-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="111dc-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="111dc-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="111dc-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
