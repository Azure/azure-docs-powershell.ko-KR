---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 5f76c9a1adabf69872b4d529df7e3289e4d6745b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997495"
---
# <span data-ttu-id="ea2ea-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="ea2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2ea-103">일시 중단된 Azure Site Recovery 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ea2ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea2ea-104">SYNTAX</span></span>

### <span data-ttu-id="ea2ea-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea2ea-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2ea-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ea2ea-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="ea2ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ea2ea-108">**Resume-AzRecoveryServicesAsrJob** cmdlet은 일시 중단된 Azure Site Recovery 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ea2ea-109">예제</span><span class="sxs-lookup"><span data-stu-id="ea2ea-109">EXAMPLES</span></span>

### <span data-ttu-id="ea2ea-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea2ea-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="ea2ea-111">대기 중 또는 일시 중단 상태인 경우 지정된 작업을 다시 시작하고 ASR 작업에 해당하는 업데이트된 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="ea2ea-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea2ea-112">PARAMETERS</span></span>

### <span data-ttu-id="ea2ea-113">-comment</span><span class="sxs-lookup"><span data-stu-id="ea2ea-113">-Comment</span></span>
<span data-ttu-id="ea2ea-114">작업 로그에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2ea-115">-DefaultProfile</span></span>
<span data-ttu-id="ea2ea-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ea2ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea2ea-117">-InputObject</span></span>
<span data-ttu-id="ea2ea-118">cmdlet에 대한 입력 개체: 다시 시작할 작업에 해당하는 ASR 작업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="ea2ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea2ea-119">-Name</span></span>
<span data-ttu-id="ea2ea-120">이름으로 ASR 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="ea2ea-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ea2ea-121">-Confirm</span></span>
<span data-ttu-id="ea2ea-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea2ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2ea-123">-WhatIf</span></span>
<span data-ttu-id="ea2ea-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea2ea-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea2ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2ea-126">CommonParameters</span></span>
<span data-ttu-id="ea2ea-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2ea-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea2ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2ea-129">입력</span><span class="sxs-lookup"><span data-stu-id="ea2ea-129">INPUTS</span></span>

### <span data-ttu-id="ea2ea-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea2ea-131">출력</span><span class="sxs-lookup"><span data-stu-id="ea2ea-131">OUTPUTS</span></span>

### <span data-ttu-id="ea2ea-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea2ea-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea2ea-133">NOTES</span></span>

## <span data-ttu-id="ea2ea-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2ea-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea2ea-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ea2ea-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ea2ea-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ea2ea-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
