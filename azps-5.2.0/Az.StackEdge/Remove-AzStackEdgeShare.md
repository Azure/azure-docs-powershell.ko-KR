---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358716"
---
# <span data-ttu-id="2da20-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2da20-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="2da20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2da20-102">SYNOPSIS</span></span>
<span data-ttu-id="2da20-103">디바이스에서 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-103">Removes a share from the device.</span></span>

## <span data-ttu-id="2da20-104">구문</span><span class="sxs-lookup"><span data-stu-id="2da20-104">SYNTAX</span></span>

### <span data-ttu-id="2da20-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2da20-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da20-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da20-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da20-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da20-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da20-108">설명</span><span class="sxs-lookup"><span data-stu-id="2da20-108">DESCRIPTION</span></span>
<span data-ttu-id="2da20-109">**Remove-AzStackEdgeEdgeShare** cmdlet은 Stack Edge 디바이스에 대한 연결된 에지 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="2da20-110">예제</span><span class="sxs-lookup"><span data-stu-id="2da20-110">EXAMPLES</span></span>

### <span data-ttu-id="2da20-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2da20-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="2da20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2da20-112">PARAMETERS</span></span>

### <span data-ttu-id="2da20-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2da20-113">-AsJob</span></span>
<span data-ttu-id="2da20-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2da20-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2da20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da20-115">-DefaultProfile</span></span>
<span data-ttu-id="2da20-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2da20-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2da20-117">-DeviceName</span></span>
<span data-ttu-id="2da20-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="2da20-118">Device Name</span></span>

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

### <span data-ttu-id="2da20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da20-119">-InputObject</span></span>
<span data-ttu-id="2da20-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="2da20-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2da20-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2da20-121">-Name</span></span>
<span data-ttu-id="2da20-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="2da20-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da20-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2da20-123">-PassThru</span></span>
<span data-ttu-id="2da20-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-124">returns true if successful</span></span>

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

### <span data-ttu-id="2da20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da20-125">-ResourceGroupName</span></span>
<span data-ttu-id="2da20-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2da20-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2da20-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2da20-127">-ResourceId</span></span>
<span data-ttu-id="2da20-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2da20-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da20-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2da20-129">-Confirm</span></span>
<span data-ttu-id="2da20-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da20-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da20-131">-WhatIf</span></span>
<span data-ttu-id="2da20-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2da20-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2da20-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da20-134">CommonParameters</span></span>
<span data-ttu-id="2da20-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2da20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da20-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2da20-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da20-137">입력</span><span class="sxs-lookup"><span data-stu-id="2da20-137">INPUTS</span></span>

### <span data-ttu-id="2da20-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2da20-138">System.String</span></span>

### <span data-ttu-id="2da20-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2da20-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="2da20-140">출력</span><span class="sxs-lookup"><span data-stu-id="2da20-140">OUTPUTS</span></span>

### <span data-ttu-id="2da20-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2da20-141">System.Boolean</span></span>

## <span data-ttu-id="2da20-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2da20-142">NOTES</span></span>

## <span data-ttu-id="2da20-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2da20-143">RELATED LINKS</span></span>
