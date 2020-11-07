---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704132"
---
# <span data-ttu-id="184af-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="184af-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="184af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="184af-102">SYNOPSIS</span></span>
<span data-ttu-id="184af-103">DevSpaces 컨트롤러를 업데이트 하 여 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="184af-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="184af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="184af-104">SYNTAX</span></span>

### <span data-ttu-id="184af-105">DevSpacesControllerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="184af-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184af-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="184af-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184af-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="184af-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184af-108">설명은</span><span class="sxs-lookup"><span data-stu-id="184af-108">DESCRIPTION</span></span>
<span data-ttu-id="184af-109">DevSpaces 컨트롤러를 업데이트 하 여 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="184af-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="184af-110">예제의</span><span class="sxs-lookup"><span data-stu-id="184af-110">EXAMPLES</span></span>

### <span data-ttu-id="184af-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="184af-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="184af-112">DevSpaces contoller에 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="184af-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="184af-113">변수</span><span class="sxs-lookup"><span data-stu-id="184af-113">PARAMETERS</span></span>

### <span data-ttu-id="184af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184af-114">-DefaultProfile</span></span>
<span data-ttu-id="184af-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="184af-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184af-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184af-116">-InputObject</span></span>
<span data-ttu-id="184af-117">일반적으로 파이프라인을 통해 전달 되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="184af-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="184af-118">-이름</span><span class="sxs-lookup"><span data-stu-id="184af-118">-Name</span></span>
<span data-ttu-id="184af-119">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="184af-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="184af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184af-120">-ResourceGroupName</span></span>
<span data-ttu-id="184af-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="184af-121">Resource group name</span></span>

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

### <span data-ttu-id="184af-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184af-122">-ResourceId</span></span>
<span data-ttu-id="184af-123">DevSpaces 리소스 id</span><span class="sxs-lookup"><span data-stu-id="184af-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="184af-124">태그</span><span class="sxs-lookup"><span data-stu-id="184af-124">-Tag</span></span>
<span data-ttu-id="184af-125">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="184af-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="184af-126">-확인</span><span class="sxs-lookup"><span data-stu-id="184af-126">-Confirm</span></span>
<span data-ttu-id="184af-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="184af-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184af-128">-WhatIf</span></span>
<span data-ttu-id="184af-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="184af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184af-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184af-131">CommonParameters</span></span>
<span data-ttu-id="184af-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="184af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184af-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184af-134">입력</span><span class="sxs-lookup"><span data-stu-id="184af-134">INPUTS</span></span>

### <span data-ttu-id="184af-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="184af-135">System.String</span></span>

### <span data-ttu-id="184af-136">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="184af-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="184af-137">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="184af-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="184af-138">출력</span><span class="sxs-lookup"><span data-stu-id="184af-138">OUTPUTS</span></span>

### <span data-ttu-id="184af-139">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="184af-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="184af-140">상속자</span><span class="sxs-lookup"><span data-stu-id="184af-140">NOTES</span></span>

## <span data-ttu-id="184af-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="184af-141">RELATED LINKS</span></span>
