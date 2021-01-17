---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492036"
---
# <span data-ttu-id="afc7e-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="afc7e-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="afc7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc7e-102">SYNOPSIS</span></span>
<span data-ttu-id="afc7e-103">DevSpaces 컨트롤러를 업데이트하여 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="afc7e-104">구문</span><span class="sxs-lookup"><span data-stu-id="afc7e-104">SYNTAX</span></span>

### <span data-ttu-id="afc7e-105">DevSpacesControllerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="afc7e-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc7e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc7e-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc7e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc7e-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc7e-108">설명</span><span class="sxs-lookup"><span data-stu-id="afc7e-108">DESCRIPTION</span></span>
<span data-ttu-id="afc7e-109">DevSpaces 컨트롤러를 업데이트하여 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="afc7e-110">예제</span><span class="sxs-lookup"><span data-stu-id="afc7e-110">EXAMPLES</span></span>

### <span data-ttu-id="afc7e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="afc7e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="afc7e-112">DevSpaces 컨트롤러에 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="afc7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afc7e-113">PARAMETERS</span></span>

### <span data-ttu-id="afc7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc7e-114">-DefaultProfile</span></span>
<span data-ttu-id="afc7e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc7e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afc7e-116">-InputObject</span></span>
<span data-ttu-id="afc7e-117">일반적으로 파이프라인을 통해 전달되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="afc7e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="afc7e-118">-Name</span></span>
<span data-ttu-id="afc7e-119">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="afc7e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc7e-120">-ResourceGroupName</span></span>
<span data-ttu-id="afc7e-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="afc7e-121">Resource group name</span></span>

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

### <span data-ttu-id="afc7e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc7e-122">-ResourceId</span></span>
<span data-ttu-id="afc7e-123">DevSpaces 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="afc7e-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="afc7e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="afc7e-124">-Tag</span></span>
<span data-ttu-id="afc7e-125">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc7e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afc7e-126">-Confirm</span></span>
<span data-ttu-id="afc7e-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc7e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc7e-128">-WhatIf</span></span>
<span data-ttu-id="afc7e-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="afc7e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc7e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc7e-131">CommonParameters</span></span>
<span data-ttu-id="afc7e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="afc7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc7e-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="afc7e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc7e-134">입력</span><span class="sxs-lookup"><span data-stu-id="afc7e-134">INPUTS</span></span>

### <span data-ttu-id="afc7e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="afc7e-135">System.String</span></span>

### <span data-ttu-id="afc7e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="afc7e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="afc7e-137">출력</span><span class="sxs-lookup"><span data-stu-id="afc7e-137">OUTPUTS</span></span>

### <span data-ttu-id="afc7e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="afc7e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="afc7e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="afc7e-139">NOTES</span></span>

## <span data-ttu-id="afc7e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afc7e-140">RELATED LINKS</span></span>
