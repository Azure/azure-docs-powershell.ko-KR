---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490336"
---
# <span data-ttu-id="4fcc7-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="4fcc7-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="4fcc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fcc7-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcc7-103">Active Directory 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="4fcc7-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fcc7-104">SYNTAX</span></span>

### <span data-ttu-id="4fcc7-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4fcc7-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fcc7-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcc7-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fcc7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fcc7-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fcc7-108">설명</span><span class="sxs-lookup"><span data-stu-id="4fcc7-108">DESCRIPTION</span></span>
<span data-ttu-id="4fcc7-109">Active Directory 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="4fcc7-110">예제</span><span class="sxs-lookup"><span data-stu-id="4fcc7-110">EXAMPLES</span></span>

### <span data-ttu-id="4fcc7-111">예제 1: 개체 ID로 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="4fcc7-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="4fcc7-112">테넌트에서 개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="4fcc7-113">예제 2: 파이핑하여 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="4fcc7-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="4fcc7-114">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 그룹을 Remove-AzADGroup 파이프하여 테넌트에서 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="4fcc7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fcc7-115">PARAMETERS</span></span>

### <span data-ttu-id="4fcc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcc7-116">-DefaultProfile</span></span>
<span data-ttu-id="4fcc7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fcc7-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4fcc7-118">-DisplayName</span></span>
<span data-ttu-id="4fcc7-119">제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fcc7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4fcc7-120">-Force</span></span>
<span data-ttu-id="4fcc7-121">지정한 경우 그룹 삭제 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="4fcc7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fcc7-122">-InputObject</span></span>
<span data-ttu-id="4fcc7-123">제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcc7-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4fcc7-124">-ObjectId</span></span>
<span data-ttu-id="4fcc7-125">제거할 그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcc7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fcc7-126">-PassThru</span></span>
<span data-ttu-id="4fcc7-127">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4fcc7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fcc7-128">-Confirm</span></span>
<span data-ttu-id="4fcc7-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fcc7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fcc7-130">-WhatIf</span></span>
<span data-ttu-id="4fcc7-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4fcc7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fcc7-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fcc7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcc7-133">CommonParameters</span></span>
<span data-ttu-id="4fcc7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcc7-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4fcc7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcc7-136">입력</span><span class="sxs-lookup"><span data-stu-id="4fcc7-136">INPUTS</span></span>

### <span data-ttu-id="4fcc7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4fcc7-137">System.String</span></span>

### <span data-ttu-id="4fcc7-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="4fcc7-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="4fcc7-139">출력</span><span class="sxs-lookup"><span data-stu-id="4fcc7-139">OUTPUTS</span></span>

### <span data-ttu-id="4fcc7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fcc7-140">System.Boolean</span></span>

## <span data-ttu-id="4fcc7-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fcc7-141">NOTES</span></span>

## <span data-ttu-id="4fcc7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fcc7-142">RELATED LINKS</span></span>