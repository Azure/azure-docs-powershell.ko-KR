---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056083"
---
# <span data-ttu-id="098da-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="098da-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="098da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098da-102">SYNOPSIS</span></span>
<span data-ttu-id="098da-103">Azure Site Recovery 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="098da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="098da-104">SYNTAX</span></span>

### <span data-ttu-id="098da-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="098da-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="098da-106">ByName</span><span class="sxs-lookup"><span data-stu-id="098da-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="098da-107">설명은</span><span class="sxs-lookup"><span data-stu-id="098da-107">DESCRIPTION</span></span>
<span data-ttu-id="098da-108">**AzRecoveryServicesAsrJob** cmdlet은 지정 된 Azure Site Recovery 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="098da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="098da-109">EXAMPLES</span></span>

### <span data-ttu-id="098da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="098da-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="098da-111">지정 된 작업을 중지 하려고 시도 하 고 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="098da-112">변수</span><span class="sxs-lookup"><span data-stu-id="098da-112">PARAMETERS</span></span>

### <span data-ttu-id="098da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098da-113">-DefaultProfile</span></span>
<span data-ttu-id="098da-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="098da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="098da-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="098da-115">-InputObject</span></span>
<span data-ttu-id="098da-116">Input 개체: 중지 될 ASR 작업에 해당 하는 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="098da-117">-이름</span><span class="sxs-lookup"><span data-stu-id="098da-117">-Name</span></span>
<span data-ttu-id="098da-118">ASR 작업 이름으로 중지할 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="098da-119">-확인</span><span class="sxs-lookup"><span data-stu-id="098da-119">-Confirm</span></span>
<span data-ttu-id="098da-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098da-121">-WhatIf</span></span>
<span data-ttu-id="098da-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="098da-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="098da-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="098da-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098da-124">CommonParameters</span></span>
<span data-ttu-id="098da-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="098da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098da-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="098da-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098da-127">입력</span><span class="sxs-lookup"><span data-stu-id="098da-127">INPUTS</span></span>

### <span data-ttu-id="098da-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="098da-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="098da-129">출력</span><span class="sxs-lookup"><span data-stu-id="098da-129">OUTPUTS</span></span>

### <span data-ttu-id="098da-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="098da-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="098da-131">상속자</span><span class="sxs-lookup"><span data-stu-id="098da-131">NOTES</span></span>

## <span data-ttu-id="098da-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="098da-132">RELATED LINKS</span></span>

[<span data-ttu-id="098da-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="098da-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="098da-134">다시 시작-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="098da-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="098da-135">이력서-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="098da-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
