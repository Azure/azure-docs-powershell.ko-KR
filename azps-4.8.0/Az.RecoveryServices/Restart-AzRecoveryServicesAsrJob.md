---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204470"
---
# <span data-ttu-id="9b7a8-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7a8-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9b7a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7a8-103">Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9b7a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b7a8-104">SYNTAX</span></span>

### <span data-ttu-id="9b7a8-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b7a8-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7a8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9b7a8-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b7a8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b7a8-107">DESCRIPTION</span></span>
<span data-ttu-id="9b7a8-108">**AzRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9b7a8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9b7a8-109">EXAMPLES</span></span>

### <span data-ttu-id="9b7a8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b7a8-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="9b7a8-111">지정 된 ASR 작업을 다시 시작 하 고 ASR 작업의 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="9b7a8-112">변수</span><span class="sxs-lookup"><span data-stu-id="9b7a8-112">PARAMETERS</span></span>

### <span data-ttu-id="9b7a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7a8-113">-DefaultProfile</span></span>
<span data-ttu-id="9b7a8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9b7a8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b7a8-115">-InputObject</span></span>
<span data-ttu-id="9b7a8-116">Cmdlet에 대 한 입력 개체: 다시 시작할 ASR 작업에 해당 하는 ASR 작업 개체</span><span class="sxs-lookup"><span data-stu-id="9b7a8-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="9b7a8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9b7a8-117">-Name</span></span>
<span data-ttu-id="9b7a8-118">이름을 기준으로 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="9b7a8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="9b7a8-119">-Confirm</span></span>
<span data-ttu-id="9b7a8-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7a8-121">-WhatIf</span></span>
<span data-ttu-id="9b7a8-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b7a8-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7a8-124">CommonParameters</span></span>
<span data-ttu-id="9b7a8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7a8-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b7a8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7a8-127">입력</span><span class="sxs-lookup"><span data-stu-id="9b7a8-127">INPUTS</span></span>

### <span data-ttu-id="9b7a8-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="9b7a8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b7a8-129">출력</span><span class="sxs-lookup"><span data-stu-id="9b7a8-129">OUTPUTS</span></span>

### <span data-ttu-id="9b7a8-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="9b7a8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b7a8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9b7a8-131">NOTES</span></span>

## <span data-ttu-id="9b7a8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b7a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b7a8-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7a8-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b7a8-134">이력서-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7a8-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b7a8-135">중지-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7a8-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
