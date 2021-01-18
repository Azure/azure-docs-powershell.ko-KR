---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494584"
---
# <span data-ttu-id="c978e-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c978e-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c978e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c978e-102">SYNOPSIS</span></span>
<span data-ttu-id="c978e-103">Azure Site Recovery 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="c978e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c978e-104">SYNTAX</span></span>

### <span data-ttu-id="c978e-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="c978e-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c978e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c978e-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c978e-107">설명</span><span class="sxs-lookup"><span data-stu-id="c978e-107">DESCRIPTION</span></span>
<span data-ttu-id="c978e-108">**Stop-AzRecoveryServicesAsrJob** cmdlet은 지정된 Azure Site Recovery 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="c978e-109">예제</span><span class="sxs-lookup"><span data-stu-id="c978e-109">EXAMPLES</span></span>

### <span data-ttu-id="c978e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c978e-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c978e-111">지정된 작업을 중지하려고 시도하고 업데이트된 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="c978e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c978e-112">PARAMETERS</span></span>

### <span data-ttu-id="c978e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c978e-113">-DefaultProfile</span></span>
<span data-ttu-id="c978e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c978e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c978e-115">-InputObject</span></span>
<span data-ttu-id="c978e-116">입력 개체: 중지할 ASR 작업에 해당하는 ASR 작업 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c978e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c978e-117">-Name</span></span>
<span data-ttu-id="c978e-118">ASR 작업 이름으로 중지할 ASR 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="c978e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c978e-119">-Confirm</span></span>
<span data-ttu-id="c978e-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c978e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c978e-121">-WhatIf</span></span>
<span data-ttu-id="c978e-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c978e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c978e-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c978e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c978e-124">CommonParameters</span></span>
<span data-ttu-id="c978e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c978e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c978e-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c978e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c978e-127">입력</span><span class="sxs-lookup"><span data-stu-id="c978e-127">INPUTS</span></span>

### <span data-ttu-id="c978e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c978e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c978e-129">출력</span><span class="sxs-lookup"><span data-stu-id="c978e-129">OUTPUTS</span></span>

### <span data-ttu-id="c978e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c978e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c978e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c978e-131">NOTES</span></span>

## <span data-ttu-id="c978e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c978e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c978e-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c978e-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c978e-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c978e-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c978e-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c978e-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
