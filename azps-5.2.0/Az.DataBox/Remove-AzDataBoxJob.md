---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337082"
---
# <span data-ttu-id="e5715-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e5715-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="e5715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5715-102">SYNOPSIS</span></span>
<span data-ttu-id="e5715-103">데이터 상자 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-103">Deletes the databox job</span></span>

## <span data-ttu-id="e5715-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5715-104">SYNTAX</span></span>

### <span data-ttu-id="e5715-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5715-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5715-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5715-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5715-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5715-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5715-108">설명</span><span class="sxs-lookup"><span data-stu-id="e5715-108">DESCRIPTION</span></span>
<span data-ttu-id="e5715-109">**Remove-AzDataBoxJob** cmdlet은 데이터 상자 작업 목록에서 완료된 데이터 상자 작업을 삭제하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="e5715-110">예제</span><span class="sxs-lookup"><span data-stu-id="e5715-110">EXAMPLES</span></span>

### <span data-ttu-id="e5715-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5715-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="e5715-112">지정된 데이터 상자 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="e5715-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e5715-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="e5715-114">확인 없이 지정된 데이터 상자 작업을 강제로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="e5715-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e5715-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="e5715-116">지정된 데이터 상자 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="e5715-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5715-117">PARAMETERS</span></span>

### <span data-ttu-id="e5715-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5715-118">-DefaultProfile</span></span>
<span data-ttu-id="e5715-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5715-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e5715-120">-Force</span></span>
<span data-ttu-id="e5715-121">확인 없이 강제 제거</span><span class="sxs-lookup"><span data-stu-id="e5715-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="e5715-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5715-122">-InputObject</span></span>
<span data-ttu-id="e5715-123">PSDataBoxJob 형식의 InputObject</span><span class="sxs-lookup"><span data-stu-id="e5715-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="e5715-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e5715-124">-Name</span></span>
<span data-ttu-id="e5715-125">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="e5715-125">Databox Job Name</span></span>

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

### <span data-ttu-id="e5715-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5715-126">-PassThru</span></span>
<span data-ttu-id="e5715-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="e5715-127">PassThru</span></span>

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

### <span data-ttu-id="e5715-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5715-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5715-129">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e5715-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="e5715-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5715-130">-ResourceId</span></span>
<span data-ttu-id="e5715-131">Databox 작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e5715-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="e5715-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5715-132">-Confirm</span></span>
<span data-ttu-id="e5715-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5715-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5715-134">-WhatIf</span></span>
<span data-ttu-id="e5715-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e5715-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5715-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5715-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5715-137">CommonParameters</span></span>
<span data-ttu-id="e5715-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5715-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5715-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5715-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5715-140">입력</span><span class="sxs-lookup"><span data-stu-id="e5715-140">INPUTS</span></span>

### <span data-ttu-id="e5715-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e5715-141">System.String</span></span>

## <span data-ttu-id="e5715-142">출력</span><span class="sxs-lookup"><span data-stu-id="e5715-142">OUTPUTS</span></span>

### <span data-ttu-id="e5715-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5715-143">System.Void</span></span>

## <span data-ttu-id="e5715-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5715-144">NOTES</span></span>

## <span data-ttu-id="e5715-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5715-145">RELATED LINKS</span></span>
