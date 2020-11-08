---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212791"
---
# <span data-ttu-id="74821-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="74821-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="74821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74821-102">SYNOPSIS</span></span>
<span data-ttu-id="74821-103">DevSpaces 컨트롤러를 업데이트 하 여 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="74821-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="74821-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74821-104">SYNTAX</span></span>

### <span data-ttu-id="74821-105">DevSpacesControllerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="74821-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74821-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74821-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74821-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74821-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74821-108">설명은</span><span class="sxs-lookup"><span data-stu-id="74821-108">DESCRIPTION</span></span>
<span data-ttu-id="74821-109">DevSpaces 컨트롤러를 업데이트 하 여 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="74821-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="74821-110">예제의</span><span class="sxs-lookup"><span data-stu-id="74821-110">EXAMPLES</span></span>

### <span data-ttu-id="74821-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="74821-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="74821-112">DevSpaces 컨트롤러에 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74821-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="74821-113">변수</span><span class="sxs-lookup"><span data-stu-id="74821-113">PARAMETERS</span></span>

### <span data-ttu-id="74821-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74821-114">-DefaultProfile</span></span>
<span data-ttu-id="74821-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74821-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74821-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74821-116">-InputObject</span></span>
<span data-ttu-id="74821-117">일반적으로 파이프라인을 통해 전달 되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="74821-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="74821-118">-이름</span><span class="sxs-lookup"><span data-stu-id="74821-118">-Name</span></span>
<span data-ttu-id="74821-119">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74821-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="74821-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74821-120">-ResourceGroupName</span></span>
<span data-ttu-id="74821-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="74821-121">Resource group name</span></span>

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

### <span data-ttu-id="74821-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74821-122">-ResourceId</span></span>
<span data-ttu-id="74821-123">DevSpaces 리소스 id</span><span class="sxs-lookup"><span data-stu-id="74821-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="74821-124">태그</span><span class="sxs-lookup"><span data-stu-id="74821-124">-Tag</span></span>
<span data-ttu-id="74821-125">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="74821-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="74821-126">-확인</span><span class="sxs-lookup"><span data-stu-id="74821-126">-Confirm</span></span>
<span data-ttu-id="74821-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74821-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74821-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74821-128">-WhatIf</span></span>
<span data-ttu-id="74821-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74821-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74821-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74821-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74821-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74821-131">CommonParameters</span></span>
<span data-ttu-id="74821-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74821-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74821-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74821-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74821-134">입력</span><span class="sxs-lookup"><span data-stu-id="74821-134">INPUTS</span></span>

### <span data-ttu-id="74821-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="74821-135">System.String</span></span>

### <span data-ttu-id="74821-136">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="74821-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="74821-137">출력</span><span class="sxs-lookup"><span data-stu-id="74821-137">OUTPUTS</span></span>

### <span data-ttu-id="74821-138">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="74821-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="74821-139">상속자</span><span class="sxs-lookup"><span data-stu-id="74821-139">NOTES</span></span>

## <span data-ttu-id="74821-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74821-140">RELATED LINKS</span></span>
