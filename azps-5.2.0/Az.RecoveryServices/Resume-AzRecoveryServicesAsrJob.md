---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350349"
---
# <span data-ttu-id="43517-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="43517-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="43517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43517-102">SYNOPSIS</span></span>
<span data-ttu-id="43517-103">일시 중단된 Azure Site Recovery 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="43517-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="43517-104">구문</span><span class="sxs-lookup"><span data-stu-id="43517-104">SYNTAX</span></span>

### <span data-ttu-id="43517-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="43517-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43517-106">ByName</span><span class="sxs-lookup"><span data-stu-id="43517-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43517-107">설명</span><span class="sxs-lookup"><span data-stu-id="43517-107">DESCRIPTION</span></span>
<span data-ttu-id="43517-108">**Resume-AzRecoveryServicesAsrJob** cmdlet은 일시 중단된 Azure Site Recovery 작업을 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="43517-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="43517-109">예제</span><span class="sxs-lookup"><span data-stu-id="43517-109">EXAMPLES</span></span>

### <span data-ttu-id="43517-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="43517-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="43517-111">대기 중 또는 일시 중단 상태인 경우 지정된 작업을 다시 시작하고 ASR 작업과 해당하는 업데이트된 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="43517-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="43517-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43517-112">PARAMETERS</span></span>

### <span data-ttu-id="43517-113">-Comment</span><span class="sxs-lookup"><span data-stu-id="43517-113">-Comment</span></span>
<span data-ttu-id="43517-114">작업 로그에 대한 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="43517-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="43517-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43517-115">-DefaultProfile</span></span>
<span data-ttu-id="43517-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43517-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="43517-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43517-117">-InputObject</span></span>
<span data-ttu-id="43517-118">cmdlet에 대한 입력 개체: 다시 시작할 작업에 해당하는 ASR 작업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="43517-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="43517-119">-Name</span><span class="sxs-lookup"><span data-stu-id="43517-119">-Name</span></span>
<span data-ttu-id="43517-120">이름으로 ASR 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43517-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="43517-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43517-121">-Confirm</span></span>
<span data-ttu-id="43517-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43517-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43517-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43517-123">-WhatIf</span></span>
<span data-ttu-id="43517-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43517-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43517-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43517-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43517-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43517-126">CommonParameters</span></span>
<span data-ttu-id="43517-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43517-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43517-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43517-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43517-129">입력</span><span class="sxs-lookup"><span data-stu-id="43517-129">INPUTS</span></span>

### <span data-ttu-id="43517-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="43517-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43517-131">출력</span><span class="sxs-lookup"><span data-stu-id="43517-131">OUTPUTS</span></span>

### <span data-ttu-id="43517-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="43517-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43517-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43517-133">NOTES</span></span>

## <span data-ttu-id="43517-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43517-134">RELATED LINKS</span></span>

[<span data-ttu-id="43517-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="43517-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="43517-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="43517-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="43517-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="43517-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
