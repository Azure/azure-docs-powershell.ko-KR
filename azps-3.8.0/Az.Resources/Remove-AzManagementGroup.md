---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ddbc088ec14ed09ca879ba1134292921f255784a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041855"
---
# <span data-ttu-id="30d60-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="30d60-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="30d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d60-102">SYNOPSIS</span></span>
<span data-ttu-id="30d60-103">관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="30d60-103">Removes a Management Group</span></span>

## <span data-ttu-id="30d60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30d60-104">SYNTAX</span></span>

### <span data-ttu-id="30d60-105">GroupOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="30d60-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d60-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="30d60-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30d60-107">설명은</span><span class="sxs-lookup"><span data-stu-id="30d60-107">DESCRIPTION</span></span>
<span data-ttu-id="30d60-108">**제거-AzManagementGroup** Cmdlet은 관리 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="30d60-109">예제의</span><span class="sxs-lookup"><span data-stu-id="30d60-109">EXAMPLES</span></span>

### <span data-ttu-id="30d60-110">예제 1-관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="30d60-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="30d60-111">예제 2-파이핑 PSManagementGroup 개체를 기준으로 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="30d60-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="30d60-112">변수</span><span class="sxs-lookup"><span data-stu-id="30d60-112">PARAMETERS</span></span>

### <span data-ttu-id="30d60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d60-113">-DefaultProfile</span></span>
<span data-ttu-id="30d60-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d60-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="30d60-115">-GroupName</span></span>
<span data-ttu-id="30d60-116">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="30d60-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d60-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30d60-117">-InputObject</span></span>
<span data-ttu-id="30d60-118">Get 전화의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="30d60-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="30d60-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30d60-119">-PassThru</span></span>
<span data-ttu-id="30d60-120">성공적으로 실행 되는 경우 반환 `true`</span><span class="sxs-lookup"><span data-stu-id="30d60-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="30d60-121">-확인</span><span class="sxs-lookup"><span data-stu-id="30d60-121">-Confirm</span></span>
<span data-ttu-id="30d60-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d60-123">-WhatIf</span></span>
<span data-ttu-id="30d60-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d60-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d60-126">CommonParameters</span></span>
<span data-ttu-id="30d60-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d60-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30d60-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d60-129">입력</span><span class="sxs-lookup"><span data-stu-id="30d60-129">INPUTS</span></span>

### <span data-ttu-id="30d60-130">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="30d60-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="30d60-131">출력</span><span class="sxs-lookup"><span data-stu-id="30d60-131">OUTPUTS</span></span>

### <span data-ttu-id="30d60-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="30d60-132">System.Boolean</span></span>

## <span data-ttu-id="30d60-133">상속자</span><span class="sxs-lookup"><span data-stu-id="30d60-133">NOTES</span></span>

## <span data-ttu-id="30d60-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30d60-134">RELATED LINKS</span></span>
