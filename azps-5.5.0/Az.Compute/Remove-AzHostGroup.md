---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204856"
---
# <span data-ttu-id="140c4-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="140c4-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="140c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="140c4-102">SYNOPSIS</span></span>
<span data-ttu-id="140c4-103">호스트 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-103">Removes a host group.</span></span>

## <span data-ttu-id="140c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="140c4-104">SYNTAX</span></span>

### <span data-ttu-id="140c4-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="140c4-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="140c4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="140c4-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="140c4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="140c4-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="140c4-108">설명</span><span class="sxs-lookup"><span data-stu-id="140c4-108">DESCRIPTION</span></span>
<span data-ttu-id="140c4-109">이 cmdlet은 호스트 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="140c4-110">예제</span><span class="sxs-lookup"><span data-stu-id="140c4-110">EXAMPLES</span></span>

### <span data-ttu-id="140c4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="140c4-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="140c4-112">이 명령은 주어진 호스트 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="140c4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="140c4-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="140c4-114">이 명령은 주어진 호스트 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-114">This command removes the given host group.</span></span>

## <span data-ttu-id="140c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="140c4-115">PARAMETERS</span></span>

### <span data-ttu-id="140c4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="140c4-116">-AsJob</span></span>
<span data-ttu-id="140c4-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="140c4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="140c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140c4-118">-DefaultProfile</span></span>
<span data-ttu-id="140c4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="140c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="140c4-120">-InputObject</span></span>
<span data-ttu-id="140c4-121">호스트 그룹의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="140c4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="140c4-122">-Name</span></span>
<span data-ttu-id="140c4-123">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-123">The name of the host group.</span></span>

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

### <span data-ttu-id="140c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="140c4-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="140c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="140c4-126">-ResourceId</span></span>
<span data-ttu-id="140c4-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="140c4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="140c4-128">-Confirm</span></span>
<span data-ttu-id="140c4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="140c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="140c4-130">-WhatIf</span></span>
<span data-ttu-id="140c4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="140c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="140c4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="140c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140c4-133">CommonParameters</span></span>
<span data-ttu-id="140c4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="140c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140c4-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="140c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140c4-136">입력</span><span class="sxs-lookup"><span data-stu-id="140c4-136">INPUTS</span></span>

### <span data-ttu-id="140c4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="140c4-137">System.String</span></span>

### <span data-ttu-id="140c4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="140c4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="140c4-139">출력</span><span class="sxs-lookup"><span data-stu-id="140c4-139">OUTPUTS</span></span>

### <span data-ttu-id="140c4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="140c4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="140c4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="140c4-141">NOTES</span></span>

## <span data-ttu-id="140c4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="140c4-142">RELATED LINKS</span></span>
