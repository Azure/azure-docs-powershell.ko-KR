---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535307"
---
# <span data-ttu-id="04f1f-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="04f1f-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="04f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="04f1f-103">일괄 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04f1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04f1f-104">SYNTAX</span></span>

### <span data-ttu-id="04f1f-105">I</span><span class="sxs-lookup"><span data-stu-id="04f1f-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f1f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="04f1f-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="04f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="04f1f-108">**제거-AzureBatchTask** Cmdlet은 Azure Batch 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="04f1f-109">*Force* 매개 변수를 지정 하지 않는 한이 cmdlet은 확인을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="04f1f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="04f1f-110">EXAMPLES</span></span>

### <span data-ttu-id="04f1f-111">예제 1: ID를 기준으로 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="04f1f-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="04f1f-112">이 명령은 ID Task23가 있는 작업 아래에 id가 포함 된 000001를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="04f1f-113">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="04f1f-114">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="04f1f-115">예제 2: 확인 하지 않고 파이프라인을 사용 하 여 일괄 처리 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="04f1f-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="04f1f-116">이 명령은 **Get-AzureBatchTask** cmdlet을 사용 하 여 id 작업이 있는 작업에서 id Task26이 있는 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="04f1f-117">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="04f1f-118">이 명령은 해당 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-118">The command deletes that task.</span></span>
<span data-ttu-id="04f1f-119">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="04f1f-120">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="04f1f-121">변수</span><span class="sxs-lookup"><span data-stu-id="04f1f-121">PARAMETERS</span></span>

### <span data-ttu-id="04f1f-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="04f1f-122">-BatchContext</span></span>
<span data-ttu-id="04f1f-123">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="04f1f-124">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="04f1f-125">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="04f1f-126">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="04f1f-127">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f1f-128">-DefaultProfile</span></span>
<span data-ttu-id="04f1f-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04f1f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="04f1f-130">-Force</span></span>
<span data-ttu-id="04f1f-131">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-132">-Id</span><span class="sxs-lookup"><span data-stu-id="04f1f-132">-Id</span></span>
<span data-ttu-id="04f1f-133">이 cmdlet이 삭제 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="04f1f-134">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04f1f-135">-InputObject</span></span>
<span data-ttu-id="04f1f-136">이 cmdlet이 삭제 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="04f1f-137">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="04f1f-138">-JobId</span></span>
<span data-ttu-id="04f1f-139">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="04f1f-140">-Confirm</span></span>
<span data-ttu-id="04f1f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f1f-142">-WhatIf</span></span>
<span data-ttu-id="04f1f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f1f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f1f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f1f-145">CommonParameters</span></span>
<span data-ttu-id="04f1f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f1f-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f1f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f1f-148">입력</span><span class="sxs-lookup"><span data-stu-id="04f1f-148">INPUTS</span></span>

### <span data-ttu-id="04f1f-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="04f1f-149">BatchAccountContext</span></span>
<span data-ttu-id="04f1f-150">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="04f1f-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="04f1f-151">PSCloudTask</span></span>
<span data-ttu-id="04f1f-152">' InputObject ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f1f-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="04f1f-153">출력</span><span class="sxs-lookup"><span data-stu-id="04f1f-153">OUTPUTS</span></span>

## <span data-ttu-id="04f1f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="04f1f-154">NOTES</span></span>

## <span data-ttu-id="04f1f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04f1f-155">RELATED LINKS</span></span>

[<span data-ttu-id="04f1f-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="04f1f-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="04f1f-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="04f1f-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="04f1f-158">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="04f1f-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="04f1f-159">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="04f1f-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="04f1f-160">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="04f1f-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="04f1f-161">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="04f1f-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


