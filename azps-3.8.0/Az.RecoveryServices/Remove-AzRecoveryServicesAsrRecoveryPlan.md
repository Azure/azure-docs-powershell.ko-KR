---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042639"
---
# <span data-ttu-id="71b26-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b26-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="71b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b26-102">SYNOPSIS</span></span>
<span data-ttu-id="71b26-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 복구 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="71b26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71b26-104">SYNTAX</span></span>

### <span data-ttu-id="71b26-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="71b26-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b26-106">ByName</span><span class="sxs-lookup"><span data-stu-id="71b26-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b26-107">설명은</span><span class="sxs-lookup"><span data-stu-id="71b26-107">DESCRIPTION</span></span>
<span data-ttu-id="71b26-108">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet은 복구 서비스 자격 증명 모음에서 지정 된 복구 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="71b26-109">예제의</span><span class="sxs-lookup"><span data-stu-id="71b26-109">EXAMPLES</span></span>

### <span data-ttu-id="71b26-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="71b26-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="71b26-111">지정 된 복구 계획의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="71b26-112">변수</span><span class="sxs-lookup"><span data-stu-id="71b26-112">PARAMETERS</span></span>

### <span data-ttu-id="71b26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b26-113">-DefaultProfile</span></span>
<span data-ttu-id="71b26-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71b26-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71b26-115">-InputObject</span></span>
<span data-ttu-id="71b26-116">Cmdlet에 대 한 입력 개체: 삭제할 복구 계획에 해당 하는 ASR 복구 계획 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="71b26-117">-이름</span><span class="sxs-lookup"><span data-stu-id="71b26-117">-Name</span></span>
<span data-ttu-id="71b26-118">삭제할 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="71b26-119">-확인</span><span class="sxs-lookup"><span data-stu-id="71b26-119">-Confirm</span></span>
<span data-ttu-id="71b26-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b26-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b26-121">-WhatIf</span></span>
<span data-ttu-id="71b26-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71b26-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b26-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b26-124">CommonParameters</span></span>
<span data-ttu-id="71b26-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b26-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b26-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="71b26-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b26-127">입력</span><span class="sxs-lookup"><span data-stu-id="71b26-127">INPUTS</span></span>

### <span data-ttu-id="71b26-128">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="71b26-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="71b26-129">출력</span><span class="sxs-lookup"><span data-stu-id="71b26-129">OUTPUTS</span></span>

### <span data-ttu-id="71b26-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="71b26-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71b26-131">상속자</span><span class="sxs-lookup"><span data-stu-id="71b26-131">NOTES</span></span>

## <span data-ttu-id="71b26-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71b26-132">RELATED LINKS</span></span>

[<span data-ttu-id="71b26-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b26-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="71b26-134">새로운 AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b26-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="71b26-135">업데이트-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b26-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


