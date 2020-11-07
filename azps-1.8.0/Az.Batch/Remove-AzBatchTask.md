---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701833"
---
# <span data-ttu-id="6b5d4-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b5d4-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="6b5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5d4-103">일괄 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="6b5d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b5d4-104">SYNTAX</span></span>

### <span data-ttu-id="6b5d4-105">I</span><span class="sxs-lookup"><span data-stu-id="6b5d4-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b5d4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6b5d4-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b5d4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6b5d4-107">DESCRIPTION</span></span>
<span data-ttu-id="6b5d4-108">**AzBatchTask** Cmdlet은 Azure Batch 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="6b5d4-109">*Force* 매개 변수를 지정 하지 않는 한이 cmdlet은 확인을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="6b5d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6b5d4-110">EXAMPLES</span></span>

### <span data-ttu-id="6b5d4-111">예제 1: ID를 기준으로 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="6b5d4-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="6b5d4-112">이 명령은 ID Task23가 있는 작업 아래에 id가 포함 된 000001를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6b5d4-113">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6b5d4-114">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6b5d4-115">예제 2: 확인 하지 않고 파이프라인을 사용 하 여 일괄 처리 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="6b5d4-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="6b5d4-116">이 명령은 **000001 cmdlet을 사용 하 여 Id** 작업이 있는 작업에서 id Task26 인 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="6b5d4-117">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6b5d4-118">이 명령은 해당 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-118">The command deletes that task.</span></span>
<span data-ttu-id="6b5d4-119">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6b5d4-120">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6b5d4-121">변수</span><span class="sxs-lookup"><span data-stu-id="6b5d4-121">PARAMETERS</span></span>

### <span data-ttu-id="6b5d4-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b5d4-122">-BatchContext</span></span>
<span data-ttu-id="6b5d4-123">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b5d4-124">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b5d4-125">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b5d4-126">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b5d4-127">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b5d4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b5d4-128">-DefaultProfile</span></span>
<span data-ttu-id="6b5d4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b5d4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6b5d4-130">-Force</span></span>
<span data-ttu-id="6b5d4-131">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5d4-132">-Id</span><span class="sxs-lookup"><span data-stu-id="6b5d4-132">-Id</span></span>
<span data-ttu-id="6b5d4-133">이 cmdlet이 삭제 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6b5d4-134">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="6b5d4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b5d4-135">-InputObject</span></span>
<span data-ttu-id="6b5d4-136">이 cmdlet이 삭제 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6b5d4-137">**Pscloudtask** 개체를 가져오려면 Get-AzBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="6b5d4-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b5d4-138">-JobId</span></span>
<span data-ttu-id="6b5d4-139">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="6b5d4-140">-확인</span><span class="sxs-lookup"><span data-stu-id="6b5d4-140">-Confirm</span></span>
<span data-ttu-id="6b5d4-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5d4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b5d4-142">-WhatIf</span></span>
<span data-ttu-id="6b5d4-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b5d4-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5d4-145">CommonParameters</span></span>
<span data-ttu-id="6b5d4-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b5d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5d4-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b5d4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5d4-148">입력</span><span class="sxs-lookup"><span data-stu-id="6b5d4-148">INPUTS</span></span>

### <span data-ttu-id="6b5d4-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b5d4-149">System.String</span></span>

### <span data-ttu-id="6b5d4-150">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="6b5d4-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="6b5d4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b5d4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b5d4-152">출력</span><span class="sxs-lookup"><span data-stu-id="6b5d4-152">OUTPUTS</span></span>

### <span data-ttu-id="6b5d4-153">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6b5d4-153">System.Void</span></span>

## <span data-ttu-id="6b5d4-154">상속자</span><span class="sxs-lookup"><span data-stu-id="6b5d4-154">NOTES</span></span>

## <span data-ttu-id="6b5d4-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b5d4-155">RELATED LINKS</span></span>

[<span data-ttu-id="6b5d4-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b5d4-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6b5d4-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b5d4-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6b5d4-158">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b5d4-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6b5d4-159">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b5d4-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6b5d4-160">중지-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b5d4-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6b5d4-161">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b5d4-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


