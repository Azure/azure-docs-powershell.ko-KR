---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192844"
---
# <span data-ttu-id="6396f-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6396f-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="6396f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6396f-102">SYNOPSIS</span></span>
<span data-ttu-id="6396f-103">Azure Site Recovery 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="6396f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6396f-104">SYNTAX</span></span>

### <span data-ttu-id="6396f-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="6396f-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6396f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6396f-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6396f-107">설명</span><span class="sxs-lookup"><span data-stu-id="6396f-107">DESCRIPTION</span></span>
<span data-ttu-id="6396f-108">**Restart-AzRecoveryServicesAsrJob** cmdlet은 Azure Site Recovery 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="6396f-109">예제</span><span class="sxs-lookup"><span data-stu-id="6396f-109">EXAMPLES</span></span>

### <span data-ttu-id="6396f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6396f-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="6396f-111">지정된 ASR 작업을 다시 시작하고 ASR 작업의 업데이트된 ASR 작업 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="6396f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6396f-112">PARAMETERS</span></span>

### <span data-ttu-id="6396f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6396f-113">-DefaultProfile</span></span>
<span data-ttu-id="6396f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6396f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6396f-115">-InputObject</span></span>
<span data-ttu-id="6396f-116">cmdlet에 대한 입력 개체: 다시 시작할 ASR 작업의 ASR 작업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="6396f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6396f-117">-Name</span></span>
<span data-ttu-id="6396f-118">이름으로 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="6396f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6396f-119">-Confirm</span></span>
<span data-ttu-id="6396f-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6396f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6396f-121">-WhatIf</span></span>
<span data-ttu-id="6396f-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6396f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6396f-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6396f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6396f-124">CommonParameters</span></span>
<span data-ttu-id="6396f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6396f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6396f-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6396f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6396f-127">입력</span><span class="sxs-lookup"><span data-stu-id="6396f-127">INPUTS</span></span>

### <span data-ttu-id="6396f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6396f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6396f-129">출력</span><span class="sxs-lookup"><span data-stu-id="6396f-129">OUTPUTS</span></span>

### <span data-ttu-id="6396f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6396f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6396f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6396f-131">NOTES</span></span>

## <span data-ttu-id="6396f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6396f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6396f-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6396f-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="6396f-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6396f-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="6396f-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6396f-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
