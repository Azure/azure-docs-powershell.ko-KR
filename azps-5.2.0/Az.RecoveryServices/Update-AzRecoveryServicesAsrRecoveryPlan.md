---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364750"
---
# <span data-ttu-id="5bc3b-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc3b-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="5bc3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc3b-103">Azure Site Recovery 계획의 콘텐츠를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="5bc3b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bc3b-104">SYNTAX</span></span>

### <span data-ttu-id="5bc3b-105">ByRPObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="5bc3b-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc3b-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="5bc3b-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc3b-107">설명</span><span class="sxs-lookup"><span data-stu-id="5bc3b-107">DESCRIPTION</span></span>
<span data-ttu-id="5bc3b-108">**Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet은 지정된 ASR 복구 계획 개체 또는 ASR 복구 계획 정의 json 파일의 내용을 사용하여 복구 계획의 콘텐츠를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="5bc3b-109">예제</span><span class="sxs-lookup"><span data-stu-id="5bc3b-109">EXAMPLES</span></span>

### <span data-ttu-id="5bc3b-110">예제 1: 복구 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="5bc3b-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="5bc3b-111">지정된 ASR 복구 계획 개체의 내용을 사용하여 복구 계획을 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5bc3b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc3b-112">PARAMETERS</span></span>

### <span data-ttu-id="5bc3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc3b-113">-DefaultProfile</span></span>
<span data-ttu-id="5bc3b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5bc3b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bc3b-115">-InputObject</span></span>
<span data-ttu-id="5bc3b-116">cmdlet에 대한 입력 개체: ASR 복구 계획 개체를 지정합니다. 이 개체에서 참조하는 복구 계획을 업데이트하는 데 사용되는 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc3b-117">-Path</span><span class="sxs-lookup"><span data-stu-id="5bc3b-117">-Path</span></span>
<span data-ttu-id="5bc3b-118">복구 계획을 업데이트하는 데 사용되는 복구 계획 정의 json 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc3b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bc3b-119">-Confirm</span></span>
<span data-ttu-id="5bc3b-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc3b-121">-WhatIf</span></span>
<span data-ttu-id="5bc3b-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5bc3b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bc3b-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc3b-124">CommonParameters</span></span>
<span data-ttu-id="5bc3b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc3b-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bc3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc3b-127">입력</span><span class="sxs-lookup"><span data-stu-id="5bc3b-127">INPUTS</span></span>

### <span data-ttu-id="5bc3b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc3b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="5bc3b-129">출력</span><span class="sxs-lookup"><span data-stu-id="5bc3b-129">OUTPUTS</span></span>

### <span data-ttu-id="5bc3b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5bc3b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5bc3b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bc3b-131">NOTES</span></span>

## <span data-ttu-id="5bc3b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bc3b-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bc3b-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc3b-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5bc3b-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc3b-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5bc3b-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc3b-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
