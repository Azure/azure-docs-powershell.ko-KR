---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: b6fb42ccafe5b70316ea29251a87b76ea65dda7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700961"
---
# <span data-ttu-id="adbd9-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="adbd9-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="adbd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="adbd9-103">DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="adbd9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adbd9-104">SYNTAX</span></span>

### <span data-ttu-id="adbd9-105">DevSpacesControllerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="adbd9-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbd9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adbd9-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbd9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adbd9-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbd9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="adbd9-108">DESCRIPTION</span></span>
<span data-ttu-id="adbd9-109">DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="adbd9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="adbd9-110">EXAMPLES</span></span>

### <span data-ttu-id="adbd9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="adbd9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="adbd9-112">DevSpaceControllerName 라는 DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="adbd9-113">변수</span><span class="sxs-lookup"><span data-stu-id="adbd9-113">PARAMETERS</span></span>

### <span data-ttu-id="adbd9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adbd9-114">-AsJob</span></span>
<span data-ttu-id="adbd9-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="adbd9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adbd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbd9-116">-DefaultProfile</span></span>
<span data-ttu-id="adbd9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbd9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adbd9-118">-InputObject</span></span>
<span data-ttu-id="adbd9-119">일반적으로 파이프라인을 통해 전달 되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="adbd9-120">-이름</span><span class="sxs-lookup"><span data-stu-id="adbd9-120">-Name</span></span>
<span data-ttu-id="adbd9-121">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="adbd9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adbd9-122">-PassThru</span></span>
<span data-ttu-id="adbd9-123">삭제가 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="adbd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="adbd9-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="adbd9-125">Resource group name</span></span>

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

### <span data-ttu-id="adbd9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adbd9-126">-ResourceId</span></span>
<span data-ttu-id="adbd9-127">DevSpaces 리소스 id</span><span class="sxs-lookup"><span data-stu-id="adbd9-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="adbd9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="adbd9-128">-Confirm</span></span>
<span data-ttu-id="adbd9-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbd9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbd9-130">-WhatIf</span></span>
<span data-ttu-id="adbd9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbd9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbd9-133">CommonParameters</span></span>
<span data-ttu-id="adbd9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbd9-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbd9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbd9-136">입력</span><span class="sxs-lookup"><span data-stu-id="adbd9-136">INPUTS</span></span>

### <span data-ttu-id="adbd9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adbd9-137">System.String</span></span>

### <span data-ttu-id="adbd9-138">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="adbd9-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="adbd9-139">출력</span><span class="sxs-lookup"><span data-stu-id="adbd9-139">OUTPUTS</span></span>

### <span data-ttu-id="adbd9-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="adbd9-140">System.Boolean</span></span>

## <span data-ttu-id="adbd9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="adbd9-141">NOTES</span></span>

## <span data-ttu-id="adbd9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adbd9-142">RELATED LINKS</span></span>