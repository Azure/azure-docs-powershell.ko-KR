---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 5550603bc4204937e8568b50b739ef8b8fadba14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959808"
---
# <span data-ttu-id="e49cc-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e49cc-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="e49cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e49cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e49cc-103">Batch 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-103">Stops a Batch task.</span></span>

## <span data-ttu-id="e49cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="e49cc-104">SYNTAX</span></span>

### <span data-ttu-id="e49cc-105">ID</span><span class="sxs-lookup"><span data-stu-id="e49cc-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e49cc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e49cc-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e49cc-107">설명</span><span class="sxs-lookup"><span data-stu-id="e49cc-107">DESCRIPTION</span></span>
<span data-ttu-id="e49cc-108">**Stop-AzBatchTask** cmdlet은 Azure Batch 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="e49cc-109">예제</span><span class="sxs-lookup"><span data-stu-id="e49cc-109">EXAMPLES</span></span>

### <span data-ttu-id="e49cc-110">예제 1: ID로 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="e49cc-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="e49cc-111">이 명령은 ID Job-000001이 있는 작업 아래에 ID Task23이 있는 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e49cc-112">명령을 통해 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="e49cc-113">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e49cc-114">예제 2: 파이프라인을 사용하여 Batch 작업 중지</span><span class="sxs-lookup"><span data-stu-id="e49cc-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="e49cc-115">이 명령은 id Job-0000001이 있는 작업에 id Task26이 있는 batch 작업을 Get-AzBatchTask cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="e49cc-116">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 이 작업을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e49cc-117">명령은 이 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-117">The command stops that task.</span></span>

## <span data-ttu-id="e49cc-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e49cc-118">PARAMETERS</span></span>

### <span data-ttu-id="e49cc-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e49cc-119">-BatchContext</span></span>
<span data-ttu-id="e49cc-120">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e49cc-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e49cc-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e49cc-123">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e49cc-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e49cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49cc-125">-DefaultProfile</span></span>
<span data-ttu-id="e49cc-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49cc-127">-Id</span><span class="sxs-lookup"><span data-stu-id="e49cc-127">-Id</span></span>
<span data-ttu-id="e49cc-128">이 cmdlet이 중지하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49cc-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="e49cc-129">-JobId</span></span>
<span data-ttu-id="e49cc-130">작업을 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49cc-131">-Task</span><span class="sxs-lookup"><span data-stu-id="e49cc-131">-Task</span></span>
<span data-ttu-id="e49cc-132">이 cmdlet이 중지하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="e49cc-133">**PSCloudTask** 개체를 얻은 경우 Get-AzBatchTask cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e49cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49cc-134">CommonParameters</span></span>
<span data-ttu-id="e49cc-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e49cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49cc-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e49cc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49cc-137">입력</span><span class="sxs-lookup"><span data-stu-id="e49cc-137">INPUTS</span></span>

### <span data-ttu-id="e49cc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e49cc-138">System.String</span></span>

### <span data-ttu-id="e49cc-139">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="e49cc-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="e49cc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e49cc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e49cc-141">출력</span><span class="sxs-lookup"><span data-stu-id="e49cc-141">OUTPUTS</span></span>

### <span data-ttu-id="e49cc-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="e49cc-142">System.Void</span></span>

## <span data-ttu-id="e49cc-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e49cc-143">NOTES</span></span>

## <span data-ttu-id="e49cc-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e49cc-144">RELATED LINKS</span></span>

[<span data-ttu-id="e49cc-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e49cc-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="e49cc-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e49cc-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="e49cc-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e49cc-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="e49cc-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e49cc-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
