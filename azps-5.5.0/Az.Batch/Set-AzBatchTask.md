---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205189"
---
# <span data-ttu-id="7fd91-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="7fd91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd91-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd91-103">작업의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="7fd91-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fd91-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd91-105">설명</span><span class="sxs-lookup"><span data-stu-id="7fd91-105">DESCRIPTION</span></span>
<span data-ttu-id="7fd91-106">**Set-AzBatchTask** cmdlet은 Azure Batch 서비스에서 태스크의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="7fd91-107">Get-AzBatchTask cmdlet을 사용하여 **PSCloudTask 개체를** 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="7fd91-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용하여 Batch 서비스에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="7fd91-109">예제</span><span class="sxs-lookup"><span data-stu-id="7fd91-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd91-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="7fd91-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="7fd91-111">첫 번째 명령은 **Get-AzBatchTask를** 사용하여 작업을 수행한 다음, $Task 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="7fd91-112">다음 두 명령은 작업의 제약 조건을 $Task.</span><span class="sxs-lookup"><span data-stu-id="7fd91-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="7fd91-113">마지막 명령은 Batch 서비스의 로컬 개체와 일치하게 Batch 서비스를 $Task.</span><span class="sxs-lookup"><span data-stu-id="7fd91-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="7fd91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fd91-114">PARAMETERS</span></span>

### <span data-ttu-id="7fd91-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7fd91-115">-BatchContext</span></span>
<span data-ttu-id="7fd91-116">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7fd91-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7fd91-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7fd91-119">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7fd91-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7fd91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd91-121">-DefaultProfile</span></span>
<span data-ttu-id="7fd91-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd91-123">-Task</span><span class="sxs-lookup"><span data-stu-id="7fd91-123">-Task</span></span>
<span data-ttu-id="7fd91-124">이 cmdlet이 Batch 서비스를 업데이트하는 **PSCloudTask를** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="7fd91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd91-125">CommonParameters</span></span>
<span data-ttu-id="7fd91-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd91-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fd91-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd91-128">입력</span><span class="sxs-lookup"><span data-stu-id="7fd91-128">INPUTS</span></span>

### <span data-ttu-id="7fd91-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="7fd91-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7fd91-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7fd91-131">출력</span><span class="sxs-lookup"><span data-stu-id="7fd91-131">OUTPUTS</span></span>

### <span data-ttu-id="7fd91-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="7fd91-132">System.Void</span></span>

## <span data-ttu-id="7fd91-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fd91-133">NOTES</span></span>

## <span data-ttu-id="7fd91-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fd91-134">RELATED LINKS</span></span>

[<span data-ttu-id="7fd91-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="7fd91-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7fd91-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7fd91-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="7fd91-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="7fd91-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7fd91-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="7fd91-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7fd91-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
