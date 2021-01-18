---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495708"
---
# <span data-ttu-id="374a7-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="374a7-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="374a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="374a7-102">SYNOPSIS</span></span>
<span data-ttu-id="374a7-103">작업이 취소 가능한 상태인 경우 진행되는 데이터 상자 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="374a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="374a7-104">SYNTAX</span></span>

### <span data-ttu-id="374a7-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="374a7-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="374a7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="374a7-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="374a7-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="374a7-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="374a7-108">설명</span><span class="sxs-lookup"><span data-stu-id="374a7-108">DESCRIPTION</span></span>
<span data-ttu-id="374a7-109">**Stop-AzDataBoxJob** cmdlet은 데이터 상자 작업을 취소하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="374a7-110">예제</span><span class="sxs-lookup"><span data-stu-id="374a7-110">EXAMPLES</span></span>

### <span data-ttu-id="374a7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="374a7-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="374a7-112">지정된 데이터 상자 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="374a7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="374a7-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="374a7-114">확인 없이 지정된 데이터 상자 작업을 강제로 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="374a7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="374a7-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="374a7-116">지정된 데이터 상자 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="374a7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="374a7-117">PARAMETERS</span></span>

### <span data-ttu-id="374a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374a7-118">-DefaultProfile</span></span>
<span data-ttu-id="374a7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="374a7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="374a7-120">-Force</span></span>
<span data-ttu-id="374a7-121">확인 없이 강제 중지</span><span class="sxs-lookup"><span data-stu-id="374a7-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="374a7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="374a7-122">-InputObject</span></span>
<span data-ttu-id="374a7-123">PSDataBoxJob 형식의 InputObject</span><span class="sxs-lookup"><span data-stu-id="374a7-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="374a7-124">-Name</span></span>
<span data-ttu-id="374a7-125">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="374a7-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="374a7-126">-PassThru</span></span>
<span data-ttu-id="374a7-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="374a7-127">PassThru</span></span>

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

### <span data-ttu-id="374a7-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="374a7-128">-Reason</span></span>
<span data-ttu-id="374a7-129">취소 이유</span><span class="sxs-lookup"><span data-stu-id="374a7-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="374a7-130">-ResourceGroupName</span></span>
<span data-ttu-id="374a7-131">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="374a7-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="374a7-132">-ResourceId</span></span>
<span data-ttu-id="374a7-133">Databox 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="374a7-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="374a7-134">-Confirm</span></span>
<span data-ttu-id="374a7-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="374a7-136">-WhatIf</span></span>
<span data-ttu-id="374a7-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="374a7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="374a7-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374a7-139">CommonParameters</span></span>
<span data-ttu-id="374a7-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="374a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374a7-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="374a7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374a7-142">입력</span><span class="sxs-lookup"><span data-stu-id="374a7-142">INPUTS</span></span>

### <span data-ttu-id="374a7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="374a7-143">System.String</span></span>

## <span data-ttu-id="374a7-144">출력</span><span class="sxs-lookup"><span data-stu-id="374a7-144">OUTPUTS</span></span>

### <span data-ttu-id="374a7-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="374a7-145">System.Void</span></span>

## <span data-ttu-id="374a7-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="374a7-146">NOTES</span></span>

## <span data-ttu-id="374a7-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="374a7-147">RELATED LINKS</span></span>
