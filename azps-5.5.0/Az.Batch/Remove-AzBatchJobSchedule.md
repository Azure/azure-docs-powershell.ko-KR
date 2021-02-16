---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199532"
---
# <span data-ttu-id="e22a7-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e22a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e22a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e22a7-103">Batch 작업 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="e22a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e22a7-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22a7-105">설명</span><span class="sxs-lookup"><span data-stu-id="e22a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e22a7-106">**Remove-AzBatchJobSchedule** cmdlet은 Azure Batch 작업 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="e22a7-107">예제</span><span class="sxs-lookup"><span data-stu-id="e22a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e22a7-108">예제 1: Batch 작업 일정 삭제</span><span class="sxs-lookup"><span data-stu-id="e22a7-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="e22a7-109">이 명령은 MyJobSchedule ID가 있는 작업 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="e22a7-110">이 명령은 작업을 삭제하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="e22a7-111">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e22a7-112">예제 2: 파이프라인을 사용하여 확인 없이 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="e22a7-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="e22a7-113">이 명령은 Get-AzBatchJobSchedule cmdlet을 사용하여 MyJobSchedule ID가 있는 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="e22a7-114">이 명령은 파이프라인 연산자를 사용하여 작업 일정을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e22a7-115">이 명령은 해당 작업 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="e22a7-116">이 명령은 Force 매개 *변수를* 포함하기 때문에 확인을 묻는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e22a7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e22a7-117">PARAMETERS</span></span>

### <span data-ttu-id="e22a7-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e22a7-118">-BatchContext</span></span>
<span data-ttu-id="e22a7-119">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e22a7-120">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e22a7-121">대신 공유 키 인증을 사용Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e22a7-122">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e22a7-123">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e22a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22a7-124">-DefaultProfile</span></span>
<span data-ttu-id="e22a7-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e22a7-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e22a7-126">-Force</span></span>
<span data-ttu-id="e22a7-127">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e22a7-128">-Id</span><span class="sxs-lookup"><span data-stu-id="e22a7-128">-Id</span></span>
<span data-ttu-id="e22a7-129">제거할 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="e22a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e22a7-130">-Confirm</span></span>
<span data-ttu-id="e22a7-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22a7-132">-WhatIf</span></span>
<span data-ttu-id="e22a7-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e22a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22a7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22a7-135">CommonParameters</span></span>
<span data-ttu-id="e22a7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e22a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22a7-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e22a7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22a7-138">입력</span><span class="sxs-lookup"><span data-stu-id="e22a7-138">INPUTS</span></span>

### <span data-ttu-id="e22a7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e22a7-139">System.String</span></span>

### <span data-ttu-id="e22a7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e22a7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e22a7-141">출력</span><span class="sxs-lookup"><span data-stu-id="e22a7-141">OUTPUTS</span></span>

### <span data-ttu-id="e22a7-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="e22a7-142">System.Void</span></span>

## <span data-ttu-id="e22a7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e22a7-143">NOTES</span></span>

## <span data-ttu-id="e22a7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e22a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="e22a7-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e22a7-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e22a7-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e22a7-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e22a7-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="e22a7-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e22a7-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


