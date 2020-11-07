---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703996"
---
# <span data-ttu-id="76c2a-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="76c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="76c2a-103">스케줄러 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76c2a-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="76c2a-106">**Get-AzureRmSchedulerJob** Cmdlet은 Azure Scheduler 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="76c2a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="76c2a-107">EXAMPLES</span></span>

## <span data-ttu-id="76c2a-108">변수</span><span class="sxs-lookup"><span data-stu-id="76c2a-108">PARAMETERS</span></span>

### <span data-ttu-id="76c2a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c2a-109">-DefaultProfile</span></span>
<span data-ttu-id="76c2a-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c2a-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="76c2a-111">-JobCollectionName</span></span>
<span data-ttu-id="76c2a-112">가져올 작업이 포함 된 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c2a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="76c2a-113">-JobName</span></span>
<span data-ttu-id="76c2a-114">가져올 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c2a-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="76c2a-115">-JobState</span></span>
<span data-ttu-id="76c2a-116">가져올 작업의 작업 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="76c2a-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76c2a-118">수</span><span class="sxs-lookup"><span data-stu-id="76c2a-118">Enabled</span></span> 
- <span data-ttu-id="76c2a-119">비활성화</span><span class="sxs-lookup"><span data-stu-id="76c2a-119">Disabled</span></span> 
- <span data-ttu-id="76c2a-120">오류</span><span class="sxs-lookup"><span data-stu-id="76c2a-120">Faulted</span></span> 
- <span data-ttu-id="76c2a-121">완료</span><span class="sxs-lookup"><span data-stu-id="76c2a-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="76c2a-123">가져올 작업의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c2a-124">CommonParameters</span></span>
<span data-ttu-id="76c2a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c2a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c2a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c2a-127">입력</span><span class="sxs-lookup"><span data-stu-id="76c2a-127">INPUTS</span></span>

### <span data-ttu-id="76c2a-128">않아야</span><span class="sxs-lookup"><span data-stu-id="76c2a-128">None</span></span>
<span data-ttu-id="76c2a-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76c2a-130">출력</span><span class="sxs-lookup"><span data-stu-id="76c2a-130">OUTPUTS</span></span>

### <span data-ttu-id="76c2a-131">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="76c2a-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="76c2a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="76c2a-132">NOTES</span></span>

## <span data-ttu-id="76c2a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c2a-133">RELATED LINKS</span></span>

[<span data-ttu-id="76c2a-134">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="76c2a-135">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="76c2a-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="76c2a-136">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="76c2a-137">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="76c2a-138">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="76c2a-139">제거-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="76c2a-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="76c2a-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="76c2a-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="76c2a-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="76c2a-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


