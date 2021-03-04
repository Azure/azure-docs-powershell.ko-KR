---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969216"
---
# <span data-ttu-id="84a55-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="84a55-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="84a55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a55-102">SYNOPSIS</span></span>
<span data-ttu-id="84a55-103">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="84a55-104">구문</span><span class="sxs-lookup"><span data-stu-id="84a55-104">SYNTAX</span></span>

### <span data-ttu-id="84a55-105">DevSpacesControllerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="84a55-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a55-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a55-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a55-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a55-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a55-108">설명</span><span class="sxs-lookup"><span data-stu-id="84a55-108">DESCRIPTION</span></span>
<span data-ttu-id="84a55-109">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="84a55-110">예제</span><span class="sxs-lookup"><span data-stu-id="84a55-110">EXAMPLES</span></span>

### <span data-ttu-id="84a55-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="84a55-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="84a55-112">devSpaceControllerName이라는 DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="84a55-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84a55-113">PARAMETERS</span></span>

### <span data-ttu-id="84a55-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84a55-114">-AsJob</span></span>
<span data-ttu-id="84a55-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84a55-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84a55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a55-116">-DefaultProfile</span></span>
<span data-ttu-id="84a55-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a55-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84a55-118">-InputObject</span></span>
<span data-ttu-id="84a55-119">일반적으로 파이프라인을 통해 전달되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="84a55-120">-Name</span><span class="sxs-lookup"><span data-stu-id="84a55-120">-Name</span></span>
<span data-ttu-id="84a55-121">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="84a55-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84a55-122">-PassThru</span></span>
<span data-ttu-id="84a55-123">삭제가 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="84a55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a55-124">-ResourceGroupName</span></span>
<span data-ttu-id="84a55-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="84a55-125">Resource group name</span></span>

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

### <span data-ttu-id="84a55-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84a55-126">-ResourceId</span></span>
<span data-ttu-id="84a55-127">DevSpaces 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="84a55-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="84a55-128">-확인</span><span class="sxs-lookup"><span data-stu-id="84a55-128">-Confirm</span></span>
<span data-ttu-id="84a55-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a55-130">-WhatIf</span></span>
<span data-ttu-id="84a55-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a55-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a55-133">CommonParameters</span></span>
<span data-ttu-id="84a55-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84a55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a55-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="84a55-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a55-136">입력</span><span class="sxs-lookup"><span data-stu-id="84a55-136">INPUTS</span></span>

### <span data-ttu-id="84a55-137">System.String</span><span class="sxs-lookup"><span data-stu-id="84a55-137">System.String</span></span>

### <span data-ttu-id="84a55-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="84a55-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="84a55-139">출력</span><span class="sxs-lookup"><span data-stu-id="84a55-139">OUTPUTS</span></span>

### <span data-ttu-id="84a55-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84a55-140">System.Boolean</span></span>

## <span data-ttu-id="84a55-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84a55-141">NOTES</span></span>

## <span data-ttu-id="84a55-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84a55-142">RELATED LINKS</span></span>
