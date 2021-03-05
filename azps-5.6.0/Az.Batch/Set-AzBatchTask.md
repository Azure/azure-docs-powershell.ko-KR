---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992950"
---
# <span data-ttu-id="02925-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="02925-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="02925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02925-102">SYNOPSIS</span></span>
<span data-ttu-id="02925-103">작업의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="02925-104">구문</span><span class="sxs-lookup"><span data-stu-id="02925-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02925-105">설명</span><span class="sxs-lookup"><span data-stu-id="02925-105">DESCRIPTION</span></span>
<span data-ttu-id="02925-106">**Set-AzBatchTask** cmdlet은 Azure Batch 서비스의 태스크 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="02925-107">**psCloudTask** 개체를 Get-AzBatchTask cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="02925-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용하여 Batch 서비스에 대한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="02925-109">예제</span><span class="sxs-lookup"><span data-stu-id="02925-109">EXAMPLES</span></span>

### <span data-ttu-id="02925-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="02925-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="02925-111">첫 번째 명령은 **Get-AzBatchTask를** 사용하여 작업을 수행한 다음, 해당 작업을 $Task 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="02925-112">다음 두 명령은 작업의 제약 조건을 $Task.</span><span class="sxs-lookup"><span data-stu-id="02925-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="02925-113">마지막 명령은 Batch 서비스를 업데이트하여 에 있는 로컬 개체와 $Task.</span><span class="sxs-lookup"><span data-stu-id="02925-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="02925-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02925-114">PARAMETERS</span></span>

### <span data-ttu-id="02925-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02925-115">-BatchContext</span></span>
<span data-ttu-id="02925-116">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02925-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="02925-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02925-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02925-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02925-119">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="02925-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02925-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02925-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02925-121">-DefaultProfile</span></span>
<span data-ttu-id="02925-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02925-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02925-123">-Task</span><span class="sxs-lookup"><span data-stu-id="02925-123">-Task</span></span>
<span data-ttu-id="02925-124">이 cmdlet이 Batch 서비스를 업데이트하는 **PSCloudTask를** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02925-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02925-125">CommonParameters</span></span>
<span data-ttu-id="02925-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02925-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02925-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02925-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02925-128">입력</span><span class="sxs-lookup"><span data-stu-id="02925-128">INPUTS</span></span>

### <span data-ttu-id="02925-129">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="02925-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="02925-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02925-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="02925-131">출력</span><span class="sxs-lookup"><span data-stu-id="02925-131">OUTPUTS</span></span>

### <span data-ttu-id="02925-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="02925-132">System.Void</span></span>

## <span data-ttu-id="02925-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02925-133">NOTES</span></span>

## <span data-ttu-id="02925-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02925-134">RELATED LINKS</span></span>

[<span data-ttu-id="02925-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="02925-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="02925-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="02925-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="02925-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="02925-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="02925-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="02925-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="02925-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="02925-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="02925-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02925-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
