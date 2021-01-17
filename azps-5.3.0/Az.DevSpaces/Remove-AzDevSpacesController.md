---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387185"
---
# <span data-ttu-id="60a0b-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="60a0b-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="60a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="60a0b-103">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="60a0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="60a0b-104">SYNTAX</span></span>

### <span data-ttu-id="60a0b-105">DevSpacesControllerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="60a0b-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a0b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a0b-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a0b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a0b-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a0b-108">설명</span><span class="sxs-lookup"><span data-stu-id="60a0b-108">DESCRIPTION</span></span>
<span data-ttu-id="60a0b-109">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="60a0b-110">예제</span><span class="sxs-lookup"><span data-stu-id="60a0b-110">EXAMPLES</span></span>

### <span data-ttu-id="60a0b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="60a0b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="60a0b-112">devSpaceControllerName이라는 DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="60a0b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a0b-113">PARAMETERS</span></span>

### <span data-ttu-id="60a0b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a0b-114">-AsJob</span></span>
<span data-ttu-id="60a0b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="60a0b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60a0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a0b-116">-DefaultProfile</span></span>
<span data-ttu-id="60a0b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a0b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60a0b-118">-InputObject</span></span>
<span data-ttu-id="60a0b-119">일반적으로 파이프라인을 통해 전달되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60a0b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60a0b-120">-Name</span></span>
<span data-ttu-id="60a0b-121">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a0b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60a0b-122">-PassThru</span></span>
<span data-ttu-id="60a0b-123">삭제에 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="60a0b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a0b-124">-ResourceGroupName</span></span>
<span data-ttu-id="60a0b-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="60a0b-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a0b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a0b-126">-ResourceId</span></span>
<span data-ttu-id="60a0b-127">DevSpaces 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="60a0b-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a0b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60a0b-128">-Confirm</span></span>
<span data-ttu-id="60a0b-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a0b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a0b-130">-WhatIf</span></span>
<span data-ttu-id="60a0b-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="60a0b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a0b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a0b-133">CommonParameters</span></span>
<span data-ttu-id="60a0b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60a0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a0b-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="60a0b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a0b-136">입력</span><span class="sxs-lookup"><span data-stu-id="60a0b-136">INPUTS</span></span>

### <span data-ttu-id="60a0b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="60a0b-137">System.String</span></span>

### <span data-ttu-id="60a0b-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="60a0b-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="60a0b-139">출력</span><span class="sxs-lookup"><span data-stu-id="60a0b-139">OUTPUTS</span></span>

### <span data-ttu-id="60a0b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60a0b-140">System.Boolean</span></span>

## <span data-ttu-id="60a0b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60a0b-141">NOTES</span></span>

## <span data-ttu-id="60a0b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60a0b-142">RELATED LINKS</span></span>
