---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056783"
---
# <span data-ttu-id="145c0-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="145c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145c0-102">SYNOPSIS</span></span>
<span data-ttu-id="145c0-103">일괄 처리 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="145c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="145c0-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="145c0-105">DESCRIPTION</span></span>
<span data-ttu-id="145c0-106">**AzBatchJob** Cmdlet은 Azure Batch 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="145c0-107">이 cmdlet은 *Force* 매개 변수를 지정 하지 않는 한 작업을 제거 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="145c0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="145c0-108">EXAMPLES</span></span>

### <span data-ttu-id="145c0-109">예제 1: 일괄 처리 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="145c0-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="145c0-110">이 명령은 ID Job-000001가 있는 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="145c0-111">이 명령은 작업을 삭제 하기 전에 확인을 요청 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="145c0-112">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="145c0-113">예제 2: 파이프라인을 사용 하 여 확인 없이 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="145c0-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="145c0-114">이 명령은 Get-AzBatchJob cmdlet을 사용 하 여 ID 작업이 있는 작업을 가져옵니다 000002.</span><span class="sxs-lookup"><span data-stu-id="145c0-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="145c0-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="145c0-116">명령이 해당 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-116">The command deletes that job.</span></span>
<span data-ttu-id="145c0-117">명령에 *Force* 매개 변수가 포함 되어 있기 때문에 확인을 요청 하는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="145c0-118">변수</span><span class="sxs-lookup"><span data-stu-id="145c0-118">PARAMETERS</span></span>

### <span data-ttu-id="145c0-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="145c0-119">-BatchContext</span></span>
<span data-ttu-id="145c0-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="145c0-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="145c0-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="145c0-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="145c0-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="145c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145c0-125">-DefaultProfile</span></span>
<span data-ttu-id="145c0-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="145c0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="145c0-127">-Force</span></span>
<span data-ttu-id="145c0-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="145c0-129">-Id</span><span class="sxs-lookup"><span data-stu-id="145c0-129">-Id</span></span>
<span data-ttu-id="145c0-130">이 cmdlet이 삭제 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="145c0-131">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="145c0-132">-확인</span><span class="sxs-lookup"><span data-stu-id="145c0-132">-Confirm</span></span>
<span data-ttu-id="145c0-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145c0-134">-WhatIf</span></span>
<span data-ttu-id="145c0-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145c0-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145c0-137">CommonParameters</span></span>
<span data-ttu-id="145c0-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="145c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145c0-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="145c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145c0-140">입력</span><span class="sxs-lookup"><span data-stu-id="145c0-140">INPUTS</span></span>

### <span data-ttu-id="145c0-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="145c0-141">System.String</span></span>

### <span data-ttu-id="145c0-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="145c0-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="145c0-143">출력</span><span class="sxs-lookup"><span data-stu-id="145c0-143">OUTPUTS</span></span>

### <span data-ttu-id="145c0-144">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="145c0-144">System.Void</span></span>

## <span data-ttu-id="145c0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="145c0-145">NOTES</span></span>

## <span data-ttu-id="145c0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="145c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="145c0-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="145c0-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="145c0-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="145c0-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="145c0-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="145c0-151">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="145c0-152">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="145c0-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="145c0-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="145c0-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
