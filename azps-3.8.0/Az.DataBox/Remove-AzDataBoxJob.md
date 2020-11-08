---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042164"
---
# <span data-ttu-id="ce8a1-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ce8a1-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="ce8a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8a1-103">Databox 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-103">Deletes the databox job</span></span>

## <span data-ttu-id="ce8a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce8a1-104">SYNTAX</span></span>

### <span data-ttu-id="ce8a1-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce8a1-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8a1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce8a1-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8a1-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce8a1-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce8a1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ce8a1-108">DESCRIPTION</span></span>
<span data-ttu-id="ce8a1-109">**AzDataBoxJob** cmdlet은 databox 작업 목록에서 완료 된 databox 작업을 삭제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="ce8a1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ce8a1-110">EXAMPLES</span></span>

### <span data-ttu-id="ce8a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce8a1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="ce8a1-112">지정 된 databox job을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="ce8a1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ce8a1-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="ce8a1-114">지정 된 databox 작업을 확인 하지 않고 강제로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="ce8a1-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="ce8a1-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="ce8a1-116">지정 된 databox job을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="ce8a1-117">변수</span><span class="sxs-lookup"><span data-stu-id="ce8a1-117">PARAMETERS</span></span>

### <span data-ttu-id="ce8a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8a1-118">-DefaultProfile</span></span>
<span data-ttu-id="ce8a1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce8a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ce8a1-120">-Force</span></span>
<span data-ttu-id="ce8a1-121">확인 하지 않고 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="ce8a1-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="ce8a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce8a1-122">-InputObject</span></span>
<span data-ttu-id="ce8a1-123">PSDataBoxJob 유형의 InputObject</span><span class="sxs-lookup"><span data-stu-id="ce8a1-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="ce8a1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="ce8a1-124">-Name</span></span>
<span data-ttu-id="ce8a1-125">Databox Job 이름</span><span class="sxs-lookup"><span data-stu-id="ce8a1-125">Databox Job Name</span></span>

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

### <span data-ttu-id="ce8a1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce8a1-126">-PassThru</span></span>
<span data-ttu-id="ce8a1-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="ce8a1-127">PassThru</span></span>

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

### <span data-ttu-id="ce8a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce8a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="ce8a1-129">Databox Job 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ce8a1-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="ce8a1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce8a1-130">-ResourceId</span></span>
<span data-ttu-id="ce8a1-131">Databox Job 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ce8a1-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="ce8a1-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ce8a1-132">-Confirm</span></span>
<span data-ttu-id="ce8a1-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce8a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce8a1-134">-WhatIf</span></span>
<span data-ttu-id="ce8a1-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce8a1-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce8a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8a1-137">CommonParameters</span></span>
<span data-ttu-id="ce8a1-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8a1-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8a1-140">입력</span><span class="sxs-lookup"><span data-stu-id="ce8a1-140">INPUTS</span></span>

### <span data-ttu-id="ce8a1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce8a1-141">System.String</span></span>

## <span data-ttu-id="ce8a1-142">출력</span><span class="sxs-lookup"><span data-stu-id="ce8a1-142">OUTPUTS</span></span>

### <span data-ttu-id="ce8a1-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ce8a1-143">System.Void</span></span>

## <span data-ttu-id="ce8a1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ce8a1-144">NOTES</span></span>

## <span data-ttu-id="ce8a1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce8a1-145">RELATED LINKS</span></span>