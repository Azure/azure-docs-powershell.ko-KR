---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703624"
---
# <span data-ttu-id="ace12-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="ace12-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="ace12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace12-102">SYNOPSIS</span></span>
<span data-ttu-id="ace12-103">스케줄러 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ace12-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ace12-105">DESCRIPTION</span></span>
<span data-ttu-id="ace12-106">**Get-AzureRmSchedulerJob** Cmdlet은 Azure Scheduler 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="ace12-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ace12-107">EXAMPLES</span></span>

## <span data-ttu-id="ace12-108">변수</span><span class="sxs-lookup"><span data-stu-id="ace12-108">PARAMETERS</span></span>

### <span data-ttu-id="ace12-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ace12-109">-JobCollectionName</span></span>
<span data-ttu-id="ace12-110">가져올 작업이 포함 된 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-110">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace12-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="ace12-111">-JobName</span></span>
<span data-ttu-id="ace12-112">가져올 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-112">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace12-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="ace12-113">-JobState</span></span>
<span data-ttu-id="ace12-114">가져올 작업의 작업 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="ace12-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ace12-116">수</span><span class="sxs-lookup"><span data-stu-id="ace12-116">Enabled</span></span> 
- <span data-ttu-id="ace12-117">비활성화</span><span class="sxs-lookup"><span data-stu-id="ace12-117">Disabled</span></span> 
- <span data-ttu-id="ace12-118">오류</span><span class="sxs-lookup"><span data-stu-id="ace12-118">Faulted</span></span> 
- <span data-ttu-id="ace12-119">완료</span><span class="sxs-lookup"><span data-stu-id="ace12-119">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace12-120">-ResourceGroupName</span></span>
<span data-ttu-id="ace12-121">가져올 작업의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-121">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace12-122">-DefaultProfile</span></span>
<span data-ttu-id="ace12-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace12-124">CommonParameters</span></span>
<span data-ttu-id="ace12-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace12-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace12-127">입력</span><span class="sxs-lookup"><span data-stu-id="ace12-127">INPUTS</span></span>

## <span data-ttu-id="ace12-128">출력</span><span class="sxs-lookup"><span data-stu-id="ace12-128">OUTPUTS</span></span>

### <span data-ttu-id="ace12-129">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ace12-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ace12-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ace12-130">NOTES</span></span>

## <span data-ttu-id="ace12-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ace12-131">RELATED LINKS</span></span>

[<span data-ttu-id="ace12-132">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ace12-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ace12-133">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ace12-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ace12-134">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ace12-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ace12-135">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ace12-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ace12-136">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ace12-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ace12-137">제거-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="ace12-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="ace12-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ace12-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ace12-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ace12-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ace12-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ace12-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ace12-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ace12-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


