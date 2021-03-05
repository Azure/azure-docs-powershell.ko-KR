---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983307"
---
# <span data-ttu-id="88fca-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="88fca-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="88fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88fca-102">SYNOPSIS</span></span>
<span data-ttu-id="88fca-103">호스트 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-103">Removes a host group.</span></span>

## <span data-ttu-id="88fca-104">구문</span><span class="sxs-lookup"><span data-stu-id="88fca-104">SYNTAX</span></span>

### <span data-ttu-id="88fca-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="88fca-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88fca-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="88fca-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88fca-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="88fca-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88fca-108">설명</span><span class="sxs-lookup"><span data-stu-id="88fca-108">DESCRIPTION</span></span>
<span data-ttu-id="88fca-109">이 cmdlet은 호스트 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="88fca-110">예제</span><span class="sxs-lookup"><span data-stu-id="88fca-110">EXAMPLES</span></span>

### <span data-ttu-id="88fca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="88fca-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="88fca-112">이 명령은 주어진 호스트 그룹을 얻게 하여 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="88fca-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="88fca-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="88fca-114">이 명령은 주어진 호스트 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-114">This command removes the given host group.</span></span>

## <span data-ttu-id="88fca-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="88fca-115">PARAMETERS</span></span>

### <span data-ttu-id="88fca-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88fca-116">-AsJob</span></span>
<span data-ttu-id="88fca-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="88fca-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88fca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fca-118">-DefaultProfile</span></span>
<span data-ttu-id="88fca-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88fca-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88fca-120">-InputObject</span></span>
<span data-ttu-id="88fca-121">호스트 그룹의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88fca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="88fca-122">-Name</span></span>
<span data-ttu-id="88fca-123">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fca-124">-ResourceGroupName</span></span>
<span data-ttu-id="88fca-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fca-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88fca-126">-ResourceId</span></span>
<span data-ttu-id="88fca-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fca-128">-확인</span><span class="sxs-lookup"><span data-stu-id="88fca-128">-Confirm</span></span>
<span data-ttu-id="88fca-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88fca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88fca-130">-WhatIf</span></span>
<span data-ttu-id="88fca-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88fca-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88fca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fca-133">CommonParameters</span></span>
<span data-ttu-id="88fca-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88fca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fca-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88fca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fca-136">입력</span><span class="sxs-lookup"><span data-stu-id="88fca-136">INPUTS</span></span>

### <span data-ttu-id="88fca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="88fca-137">System.String</span></span>

### <span data-ttu-id="88fca-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="88fca-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="88fca-139">출력</span><span class="sxs-lookup"><span data-stu-id="88fca-139">OUTPUTS</span></span>

### <span data-ttu-id="88fca-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="88fca-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="88fca-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88fca-141">NOTES</span></span>

## <span data-ttu-id="88fca-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88fca-142">RELATED LINKS</span></span>
