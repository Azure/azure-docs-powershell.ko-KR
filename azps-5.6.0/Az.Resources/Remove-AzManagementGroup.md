---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 8ef763300d530c764aefc3fa18c6bbf2a781b4b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967696"
---
# <span data-ttu-id="e080f-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e080f-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="e080f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e080f-102">SYNOPSIS</span></span>
<span data-ttu-id="e080f-103">관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e080f-103">Removes a Management Group</span></span>

## <span data-ttu-id="e080f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e080f-104">SYNTAX</span></span>

### <span data-ttu-id="e080f-105">GroupOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="e080f-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e080f-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="e080f-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e080f-107">설명</span><span class="sxs-lookup"><span data-stu-id="e080f-107">DESCRIPTION</span></span>
<span data-ttu-id="e080f-108">**Remove-AzManagementGroup** cmdlet은 관리 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="e080f-109">예제</span><span class="sxs-lookup"><span data-stu-id="e080f-109">EXAMPLES</span></span>

### <span data-ttu-id="e080f-110">예제 1: 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e080f-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="e080f-111">예제 2: PSManagementGroup 개체를 피핑하여 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e080f-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="e080f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e080f-112">PARAMETERS</span></span>

### <span data-ttu-id="e080f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e080f-113">-DefaultProfile</span></span>
<span data-ttu-id="e080f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e080f-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e080f-115">-GroupName</span></span>
<span data-ttu-id="e080f-116">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="e080f-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e080f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e080f-117">-InputObject</span></span>
<span data-ttu-id="e080f-118">호출 시작에서 입력 개체</span><span class="sxs-lookup"><span data-stu-id="e080f-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e080f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e080f-119">-PassThru</span></span>
<span data-ttu-id="e080f-120">성공적인 `true` 실행에 대한 반환</span><span class="sxs-lookup"><span data-stu-id="e080f-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="e080f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e080f-121">-Confirm</span></span>
<span data-ttu-id="e080f-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e080f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e080f-123">-WhatIf</span></span>
<span data-ttu-id="e080f-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e080f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e080f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e080f-126">CommonParameters</span></span>
<span data-ttu-id="e080f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e080f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e080f-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e080f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e080f-129">입력</span><span class="sxs-lookup"><span data-stu-id="e080f-129">INPUTS</span></span>

### <span data-ttu-id="e080f-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e080f-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e080f-131">출력</span><span class="sxs-lookup"><span data-stu-id="e080f-131">OUTPUTS</span></span>

### <span data-ttu-id="e080f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e080f-132">System.Boolean</span></span>

## <span data-ttu-id="e080f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e080f-133">NOTES</span></span>

## <span data-ttu-id="e080f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e080f-134">RELATED LINKS</span></span>
