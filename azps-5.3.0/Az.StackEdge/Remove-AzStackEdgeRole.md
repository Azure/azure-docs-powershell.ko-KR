---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376405"
---
# <span data-ttu-id="3415a-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3415a-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="3415a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3415a-102">SYNOPSIS</span></span>
<span data-ttu-id="3415a-103">디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="3415a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3415a-104">SYNTAX</span></span>

### <span data-ttu-id="3415a-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3415a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3415a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3415a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3415a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3415a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3415a-108">설명</span><span class="sxs-lookup"><span data-stu-id="3415a-108">DESCRIPTION</span></span>
<span data-ttu-id="3415a-109">**Remove-AzStackEdgeRole** cmdlet은 Stack Edge 디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="3415a-110">예제</span><span class="sxs-lookup"><span data-stu-id="3415a-110">EXAMPLES</span></span>

### <span data-ttu-id="3415a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3415a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="3415a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3415a-112">PARAMETERS</span></span>

### <span data-ttu-id="3415a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3415a-113">-AsJob</span></span>
<span data-ttu-id="3415a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3415a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3415a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3415a-115">-DefaultProfile</span></span>
<span data-ttu-id="3415a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3415a-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3415a-117">-DeviceName</span></span>
<span data-ttu-id="3415a-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="3415a-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3415a-119">-InputObject</span></span>
<span data-ttu-id="3415a-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="3415a-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3415a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3415a-121">-Name</span></span>
<span data-ttu-id="3415a-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="3415a-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3415a-123">-PassThru</span></span>
<span data-ttu-id="3415a-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-124">returns true if successful</span></span>

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

### <span data-ttu-id="3415a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3415a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3415a-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3415a-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3415a-127">-ResourceId</span></span>
<span data-ttu-id="3415a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3415a-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3415a-129">-Confirm</span></span>
<span data-ttu-id="3415a-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3415a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3415a-131">-WhatIf</span></span>
<span data-ttu-id="3415a-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3415a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3415a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3415a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3415a-134">CommonParameters</span></span>
<span data-ttu-id="3415a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3415a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3415a-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3415a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3415a-137">입력</span><span class="sxs-lookup"><span data-stu-id="3415a-137">INPUTS</span></span>

### <span data-ttu-id="3415a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3415a-138">System.String</span></span>

### <span data-ttu-id="3415a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3415a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3415a-140">출력</span><span class="sxs-lookup"><span data-stu-id="3415a-140">OUTPUTS</span></span>

### <span data-ttu-id="3415a-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3415a-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3415a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3415a-142">NOTES</span></span>

## <span data-ttu-id="3415a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3415a-143">RELATED LINKS</span></span>