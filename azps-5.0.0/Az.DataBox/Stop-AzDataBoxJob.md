---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306635"
---
# <span data-ttu-id="d5d43-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d5d43-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="d5d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d43-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d43-103">작업이 cancellable 상태인 경우 진행 중인 databox 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="d5d43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5d43-104">SYNTAX</span></span>

### <span data-ttu-id="d5d43-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5d43-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d43-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d43-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d43-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d43-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d43-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d5d43-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d43-109">**AzDataBoxJob** cmdlet은 databox 작업을 취소 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="d5d43-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5d43-110">EXAMPLES</span></span>

### <span data-ttu-id="d5d43-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5d43-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="d5d43-112">지정 된 databox job을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="d5d43-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d5d43-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="d5d43-114">지정 된 databox 작업을 확인 하지 않고 강제로 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="d5d43-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d5d43-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="d5d43-116">지정 된 databox job을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="d5d43-117">변수</span><span class="sxs-lookup"><span data-stu-id="d5d43-117">PARAMETERS</span></span>

### <span data-ttu-id="d5d43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d43-118">-DefaultProfile</span></span>
<span data-ttu-id="d5d43-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d43-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d5d43-120">-Force</span></span>
<span data-ttu-id="d5d43-121">확인 하지 않고 강제로 중지</span><span class="sxs-lookup"><span data-stu-id="d5d43-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="d5d43-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d43-122">-InputObject</span></span>
<span data-ttu-id="d5d43-123">PSDataBoxJob 유형의 InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d43-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="d5d43-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d5d43-124">-Name</span></span>
<span data-ttu-id="d5d43-125">Databox Job 이름</span><span class="sxs-lookup"><span data-stu-id="d5d43-125">Databox Job Name</span></span>

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

### <span data-ttu-id="d5d43-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5d43-126">-PassThru</span></span>
<span data-ttu-id="d5d43-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="d5d43-127">PassThru</span></span>

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

### <span data-ttu-id="d5d43-128">-이유</span><span class="sxs-lookup"><span data-stu-id="d5d43-128">-Reason</span></span>
<span data-ttu-id="d5d43-129">취소 이유</span><span class="sxs-lookup"><span data-stu-id="d5d43-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="d5d43-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d43-130">-ResourceGroupName</span></span>
<span data-ttu-id="d5d43-131">Databox Job 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d5d43-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="d5d43-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d43-132">-ResourceId</span></span>
<span data-ttu-id="d5d43-133">Databox 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d5d43-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="d5d43-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d5d43-134">-Confirm</span></span>
<span data-ttu-id="d5d43-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d43-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d43-136">-WhatIf</span></span>
<span data-ttu-id="d5d43-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5d43-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d43-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d43-139">CommonParameters</span></span>
<span data-ttu-id="d5d43-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d43-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d43-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5d43-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d43-142">입력</span><span class="sxs-lookup"><span data-stu-id="d5d43-142">INPUTS</span></span>

### <span data-ttu-id="d5d43-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5d43-143">System.String</span></span>

## <span data-ttu-id="d5d43-144">출력</span><span class="sxs-lookup"><span data-stu-id="d5d43-144">OUTPUTS</span></span>

### <span data-ttu-id="d5d43-145">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d5d43-145">System.Void</span></span>

## <span data-ttu-id="d5d43-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d5d43-146">NOTES</span></span>

## <span data-ttu-id="d5d43-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5d43-147">RELATED LINKS</span></span>
