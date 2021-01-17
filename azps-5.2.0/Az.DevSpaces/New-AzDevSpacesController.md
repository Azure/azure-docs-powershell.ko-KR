---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341066"
---
# <span data-ttu-id="668d0-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="668d0-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="668d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668d0-102">SYNOPSIS</span></span>
<span data-ttu-id="668d0-103">새 Azure DevSpaces 컨트롤러를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="668d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="668d0-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668d0-105">설명</span><span class="sxs-lookup"><span data-stu-id="668d0-105">DESCRIPTION</span></span>
<span data-ttu-id="668d0-106">새 Azure DevSpaces 컨트롤러를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="668d0-107">예제</span><span class="sxs-lookup"><span data-stu-id="668d0-107">EXAMPLES</span></span>

### <span data-ttu-id="668d0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="668d0-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="668d0-109">devSpaceName 이름으로 리소스 그룹 devSpaceResourceGroup에서 DevSpaces 컨트롤러를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="668d0-110">이 컨트롤러의 대상으로 clusterName 클러스터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="668d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="668d0-111">PARAMETERS</span></span>

### <span data-ttu-id="668d0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="668d0-112">-AsJob</span></span>
<span data-ttu-id="668d0-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="668d0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="668d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668d0-114">-DefaultProfile</span></span>
<span data-ttu-id="668d0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668d0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="668d0-116">-Name</span></span>
<span data-ttu-id="668d0-117">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668d0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668d0-118">-ResourceGroupName</span></span>
<span data-ttu-id="668d0-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668d0-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="668d0-120">-Tag</span></span>
<span data-ttu-id="668d0-121">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="668d0-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="668d0-122">-TargetClusterName</span></span>
<span data-ttu-id="668d0-123">대상 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668d0-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668d0-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="668d0-125">대상 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668d0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="668d0-126">-Confirm</span></span>
<span data-ttu-id="668d0-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668d0-128">-WhatIf</span></span>
<span data-ttu-id="668d0-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="668d0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668d0-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668d0-131">CommonParameters</span></span>
<span data-ttu-id="668d0-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="668d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668d0-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="668d0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668d0-134">입력</span><span class="sxs-lookup"><span data-stu-id="668d0-134">INPUTS</span></span>

### <span data-ttu-id="668d0-135">없음</span><span class="sxs-lookup"><span data-stu-id="668d0-135">None</span></span>

## <span data-ttu-id="668d0-136">출력</span><span class="sxs-lookup"><span data-stu-id="668d0-136">OUTPUTS</span></span>

### <span data-ttu-id="668d0-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="668d0-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="668d0-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="668d0-138">NOTES</span></span>

## <span data-ttu-id="668d0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="668d0-139">RELATED LINKS</span></span>
