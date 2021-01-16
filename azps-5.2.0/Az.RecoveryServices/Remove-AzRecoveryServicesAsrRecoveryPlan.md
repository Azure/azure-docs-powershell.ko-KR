---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355646"
---
# <span data-ttu-id="4f9a6-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f9a6-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="4f9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9a6-103">Recovery Services 자격 증명 모음에서 지정된 ASR 복구 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="4f9a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f9a6-104">SYNTAX</span></span>

### <span data-ttu-id="4f9a6-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f9a6-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f9a6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4f9a6-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f9a6-107">설명</span><span class="sxs-lookup"><span data-stu-id="4f9a6-107">DESCRIPTION</span></span>
<span data-ttu-id="4f9a6-108">**Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet은 Recovery Services 자격 증명 모음에서 지정된 복구 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="4f9a6-109">예제</span><span class="sxs-lookup"><span data-stu-id="4f9a6-109">EXAMPLES</span></span>

### <span data-ttu-id="4f9a6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f9a6-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="4f9a6-111">지정된 복구 계획의 지우기 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4f9a6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f9a6-112">PARAMETERS</span></span>

### <span data-ttu-id="4f9a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9a6-113">-DefaultProfile</span></span>
<span data-ttu-id="4f9a6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4f9a6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f9a6-115">-InputObject</span></span>
<span data-ttu-id="4f9a6-116">cmdlet에 대한 입력 개체: 삭제할 복구 계획에 해당하는 ASR 복구 계획 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f9a6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4f9a6-117">-Name</span></span>
<span data-ttu-id="4f9a6-118">삭제할 복구 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9a6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f9a6-119">-Confirm</span></span>
<span data-ttu-id="4f9a6-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9a6-121">-WhatIf</span></span>
<span data-ttu-id="4f9a6-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4f9a6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f9a6-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9a6-124">CommonParameters</span></span>
<span data-ttu-id="4f9a6-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9a6-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f9a6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9a6-127">입력</span><span class="sxs-lookup"><span data-stu-id="4f9a6-127">INPUTS</span></span>

### <span data-ttu-id="4f9a6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f9a6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="4f9a6-129">출력</span><span class="sxs-lookup"><span data-stu-id="4f9a6-129">OUTPUTS</span></span>

### <span data-ttu-id="4f9a6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4f9a6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4f9a6-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f9a6-131">NOTES</span></span>

## <span data-ttu-id="4f9a6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f9a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f9a6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f9a6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4f9a6-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f9a6-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4f9a6-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f9a6-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


