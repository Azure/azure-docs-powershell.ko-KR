---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 5e227662e8c0ce1011172eded7b218f627efbbbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009360"
---
# <span data-ttu-id="e07fc-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e07fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e07fc-103">Batch 작업 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="e07fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="e07fc-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="e07fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e07fc-106">**Remove-AzBatchJobSchedule** cmdlet은 Azure Batch 작업 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="e07fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="e07fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e07fc-108">예제 1: Batch 작업 일정 삭제</span><span class="sxs-lookup"><span data-stu-id="e07fc-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="e07fc-109">이 명령은 MyJobSchedule ID가 있는 작업 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="e07fc-110">이 명령은 작업을 삭제하기 전에 확인을 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="e07fc-111">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e07fc-112">예제 2: 파이프라인을 사용하여 확인 없이 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="e07fc-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="e07fc-113">이 명령은 id MyJobSchedule이 있는 작업 일정을 Get-AzBatchJobSchedule cmdlet을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="e07fc-114">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 작업 일정을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e07fc-115">명령은 해당 작업 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="e07fc-116">명령에 Force 매개 *변수가* 포함되어 있기 때문에 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e07fc-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e07fc-117">PARAMETERS</span></span>

### <span data-ttu-id="e07fc-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e07fc-118">-BatchContext</span></span>
<span data-ttu-id="e07fc-119">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e07fc-120">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e07fc-121">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e07fc-122">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e07fc-123">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e07fc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07fc-124">-DefaultProfile</span></span>
<span data-ttu-id="e07fc-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e07fc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e07fc-126">-Force</span></span>
<span data-ttu-id="e07fc-127">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e07fc-128">-Id</span><span class="sxs-lookup"><span data-stu-id="e07fc-128">-Id</span></span>
<span data-ttu-id="e07fc-129">제거할 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="e07fc-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e07fc-130">-Confirm</span></span>
<span data-ttu-id="e07fc-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07fc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07fc-132">-WhatIf</span></span>
<span data-ttu-id="e07fc-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07fc-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07fc-135">CommonParameters</span></span>
<span data-ttu-id="e07fc-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e07fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07fc-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e07fc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07fc-138">입력</span><span class="sxs-lookup"><span data-stu-id="e07fc-138">INPUTS</span></span>

### <span data-ttu-id="e07fc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e07fc-139">System.String</span></span>

### <span data-ttu-id="e07fc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e07fc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e07fc-141">출력</span><span class="sxs-lookup"><span data-stu-id="e07fc-141">OUTPUTS</span></span>

### <span data-ttu-id="e07fc-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="e07fc-142">System.Void</span></span>

## <span data-ttu-id="e07fc-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e07fc-143">NOTES</span></span>

## <span data-ttu-id="e07fc-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e07fc-144">RELATED LINKS</span></span>

[<span data-ttu-id="e07fc-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e07fc-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e07fc-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e07fc-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e07fc-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="e07fc-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e07fc-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


