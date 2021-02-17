---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209688"
---
# <span data-ttu-id="6685f-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6685f-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="6685f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6685f-102">SYNOPSIS</span></span>
<span data-ttu-id="6685f-103">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6685f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6685f-104">SYNTAX</span></span>

### <span data-ttu-id="6685f-105">DevSpacesControllerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6685f-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6685f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6685f-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6685f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6685f-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6685f-108">설명</span><span class="sxs-lookup"><span data-stu-id="6685f-108">DESCRIPTION</span></span>
<span data-ttu-id="6685f-109">DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6685f-110">예제</span><span class="sxs-lookup"><span data-stu-id="6685f-110">EXAMPLES</span></span>

### <span data-ttu-id="6685f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6685f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="6685f-112">devSpaceControllerName이라는 DevSpaces 컨트롤러를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="6685f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6685f-113">PARAMETERS</span></span>

### <span data-ttu-id="6685f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6685f-114">-AsJob</span></span>
<span data-ttu-id="6685f-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6685f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6685f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6685f-116">-DefaultProfile</span></span>
<span data-ttu-id="6685f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6685f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6685f-118">-InputObject</span></span>
<span data-ttu-id="6685f-119">일반적으로 파이프라인을 통해 전달되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6685f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6685f-120">-Name</span></span>
<span data-ttu-id="6685f-121">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6685f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6685f-122">-PassThru</span></span>
<span data-ttu-id="6685f-123">삭제에 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="6685f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6685f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6685f-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6685f-125">Resource group name</span></span>

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

### <span data-ttu-id="6685f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6685f-126">-ResourceId</span></span>
<span data-ttu-id="6685f-127">DevSpaces 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6685f-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="6685f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6685f-128">-Confirm</span></span>
<span data-ttu-id="6685f-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6685f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6685f-130">-WhatIf</span></span>
<span data-ttu-id="6685f-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6685f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6685f-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6685f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6685f-133">CommonParameters</span></span>
<span data-ttu-id="6685f-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6685f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6685f-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6685f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6685f-136">입력</span><span class="sxs-lookup"><span data-stu-id="6685f-136">INPUTS</span></span>

### <span data-ttu-id="6685f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6685f-137">System.String</span></span>

### <span data-ttu-id="6685f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="6685f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6685f-139">출력</span><span class="sxs-lookup"><span data-stu-id="6685f-139">OUTPUTS</span></span>

### <span data-ttu-id="6685f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6685f-140">System.Boolean</span></span>

## <span data-ttu-id="6685f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6685f-141">NOTES</span></span>

## <span data-ttu-id="6685f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6685f-142">RELATED LINKS</span></span>
