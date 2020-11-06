---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529765"
---
# <span data-ttu-id="0e8b3-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e8b3-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0e8b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8b3-103">일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e8b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e8b3-104">SYNTAX</span></span>

### <span data-ttu-id="0e8b3-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e8b3-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8b3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e8b3-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e8b3-107">DESCRIPTION</span></span>
<span data-ttu-id="0e8b3-108">**AzureRmRecoveryServicesAsrJob** cmdlet은 일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0e8b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0e8b3-109">EXAMPLES</span></span>

### <span data-ttu-id="0e8b3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e8b3-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0e8b3-111">대기 또는 일시 중단 상태에 있는 경우 지정 된 작업을 다시 시작 하 고 ASR 작업에 해당 하는 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="0e8b3-112">변수</span><span class="sxs-lookup"><span data-stu-id="0e8b3-112">PARAMETERS</span></span>

### <span data-ttu-id="0e8b3-113">-메모</span><span class="sxs-lookup"><span data-stu-id="0e8b3-113">-Comment</span></span>
<span data-ttu-id="0e8b3-114">작업 로그에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-115">-확인</span><span class="sxs-lookup"><span data-stu-id="0e8b3-115">-Confirm</span></span>
<span data-ttu-id="0e8b3-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8b3-117">-DefaultProfile</span></span>
<span data-ttu-id="0e8b3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e8b3-119">-InputObject</span></span>
<span data-ttu-id="0e8b3-120">Cmdlet에 대 한 입력 개체: 다시 시작할 작업에 해당 하는 ASR 작업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0e8b3-121">-Name</span></span>
<span data-ttu-id="0e8b3-122">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-122">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8b3-123">-WhatIf</span></span>
<span data-ttu-id="0e8b3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e8b3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8b3-126">CommonParameters</span></span>
<span data-ttu-id="0e8b3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8b3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8b3-129">입력</span><span class="sxs-lookup"><span data-stu-id="0e8b3-129">INPUTS</span></span>

### <span data-ttu-id="0e8b3-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="0e8b3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e8b3-131">출력</span><span class="sxs-lookup"><span data-stu-id="0e8b3-131">OUTPUTS</span></span>

### <span data-ttu-id="0e8b3-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="0e8b3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e8b3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0e8b3-133">NOTES</span></span>

## <span data-ttu-id="0e8b3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="0e8b3-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e8b3-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0e8b3-136">다시 시작-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e8b3-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0e8b3-137">중지-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e8b3-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
