---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325541"
---
# <span data-ttu-id="e2e4d-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e2e4d-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="e2e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e4d-103">관리 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-103">Removes a Management Group</span></span>

## <span data-ttu-id="e2e4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2e4d-104">SYNTAX</span></span>

### <span data-ttu-id="e2e4d-105">GroupOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2e4d-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e4d-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="e2e4d-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e4d-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2e4d-107">DESCRIPTION</span></span>
<span data-ttu-id="e2e4d-108">**Remove-AzManagementGroup** cmdlet은 관리 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="e2e4d-109">예제</span><span class="sxs-lookup"><span data-stu-id="e2e4d-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e4d-110">예제 1: 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e2e4d-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="e2e4d-111">예제 2: PSManagementGroup 개체를 파이핑하여 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e2e4d-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="e2e4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2e4d-112">PARAMETERS</span></span>

### <span data-ttu-id="e2e4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e4d-113">-DefaultProfile</span></span>
<span data-ttu-id="e2e4d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e4d-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e2e4d-115">-GroupName</span></span>
<span data-ttu-id="e2e4d-116">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="e2e4d-116">Management Group Id</span></span>

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

### <span data-ttu-id="e2e4d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e4d-117">-InputObject</span></span>
<span data-ttu-id="e2e4d-118">Get 호출의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="e2e4d-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="e2e4d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2e4d-119">-PassThru</span></span>
<span data-ttu-id="e2e4d-120">성공적인 `true` 실행 시 반환</span><span class="sxs-lookup"><span data-stu-id="e2e4d-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="e2e4d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2e4d-121">-Confirm</span></span>
<span data-ttu-id="e2e4d-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e4d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e4d-123">-WhatIf</span></span>
<span data-ttu-id="e2e4d-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2e4d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e4d-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e4d-126">CommonParameters</span></span>
<span data-ttu-id="e2e4d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e4d-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2e4d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e4d-129">입력</span><span class="sxs-lookup"><span data-stu-id="e2e4d-129">INPUTS</span></span>

### <span data-ttu-id="e2e4d-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e2e4d-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e2e4d-131">출력</span><span class="sxs-lookup"><span data-stu-id="e2e4d-131">OUTPUTS</span></span>

### <span data-ttu-id="e2e4d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e2e4d-132">System.Boolean</span></span>

## <span data-ttu-id="e2e4d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2e4d-133">NOTES</span></span>

## <span data-ttu-id="e2e4d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2e4d-134">RELATED LINKS</span></span>