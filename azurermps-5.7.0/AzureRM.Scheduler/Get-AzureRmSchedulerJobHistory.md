---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702513"
---
# <span data-ttu-id="c1873-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="c1873-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="c1873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1873-102">SYNOPSIS</span></span>
<span data-ttu-id="c1873-103">작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1873-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1873-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1873-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1873-105">DESCRIPTION</span></span>
<span data-ttu-id="c1873-106">**AzureRmSchedulerJobHistory** Cmdlet은 Azure Scheduler 작업에 대 한 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="c1873-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1873-107">EXAMPLES</span></span>

## <span data-ttu-id="c1873-108">변수</span><span class="sxs-lookup"><span data-stu-id="c1873-108">PARAMETERS</span></span>

### <span data-ttu-id="c1873-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1873-109">-DefaultProfile</span></span>
<span data-ttu-id="c1873-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1873-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c1873-111">-JobCollectionName</span></span>
<span data-ttu-id="c1873-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="c1873-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="c1873-113">-JobExecutionStatus</span></span>
<span data-ttu-id="c1873-114">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-114">Specifies the status of a job.</span></span>
<span data-ttu-id="c1873-115">이 cmdlet은 지정한 상태와 일치 하는 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="c1873-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c1873-117">완료</span><span class="sxs-lookup"><span data-stu-id="c1873-117">Completed</span></span> 
- <span data-ttu-id="c1873-118">못함</span><span class="sxs-lookup"><span data-stu-id="c1873-118">Failed</span></span> 
- <span data-ttu-id="c1873-119">연기</span><span class="sxs-lookup"><span data-stu-id="c1873-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1873-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="c1873-120">-JobName</span></span>
<span data-ttu-id="c1873-121">이 cmdlet이 기록을 가져오는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="c1873-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1873-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1873-123">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c1873-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1873-124">CommonParameters</span></span>
<span data-ttu-id="c1873-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1873-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1873-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1873-127">입력</span><span class="sxs-lookup"><span data-stu-id="c1873-127">INPUTS</span></span>

### <span data-ttu-id="c1873-128">않아야</span><span class="sxs-lookup"><span data-stu-id="c1873-128">None</span></span>
<span data-ttu-id="c1873-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1873-130">출력</span><span class="sxs-lookup"><span data-stu-id="c1873-130">OUTPUTS</span></span>

### <span data-ttu-id="c1873-131">PSJobHistory의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="c1873-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c1873-132">NOTES</span></span>

## <span data-ttu-id="c1873-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1873-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1873-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c1873-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


