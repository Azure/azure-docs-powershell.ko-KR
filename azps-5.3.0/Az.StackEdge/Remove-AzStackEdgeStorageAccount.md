---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376377"
---
# <span data-ttu-id="18393-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18393-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="18393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18393-102">SYNOPSIS</span></span>
<span data-ttu-id="18393-103">디바이스에 대한 Edge Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18393-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="18393-104">구문</span><span class="sxs-lookup"><span data-stu-id="18393-104">SYNTAX</span></span>

### <span data-ttu-id="18393-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="18393-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18393-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18393-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18393-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18393-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18393-108">설명</span><span class="sxs-lookup"><span data-stu-id="18393-108">DESCRIPTION</span></span>
<span data-ttu-id="18393-109">**Remove-AzStackEdgeStorageAccount** cmdlet은 Stack Edge 디바이스에 대한 연결된 Edge Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18393-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="18393-110">cmdlet에서 매개 변수로 제거할 Edge Storage 계정의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18393-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="18393-111">예제</span><span class="sxs-lookup"><span data-stu-id="18393-111">EXAMPLES</span></span>

### <span data-ttu-id="18393-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="18393-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="18393-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18393-113">PARAMETERS</span></span>

### <span data-ttu-id="18393-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18393-114">-AsJob</span></span>
<span data-ttu-id="18393-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="18393-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18393-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18393-116">-DefaultProfile</span></span>
<span data-ttu-id="18393-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18393-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18393-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="18393-118">-DeviceName</span></span>
<span data-ttu-id="18393-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="18393-119">Device Name</span></span>

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

### <span data-ttu-id="18393-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18393-120">-InputObject</span></span>
<span data-ttu-id="18393-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="18393-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18393-122">-Name</span><span class="sxs-lookup"><span data-stu-id="18393-122">-Name</span></span>
<span data-ttu-id="18393-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="18393-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18393-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18393-124">-PassThru</span></span>
<span data-ttu-id="18393-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="18393-125">returns true if successful</span></span>

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

### <span data-ttu-id="18393-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18393-126">-ResourceGroupName</span></span>
<span data-ttu-id="18393-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="18393-127">Resource Group Name</span></span>

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

### <span data-ttu-id="18393-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18393-128">-ResourceId</span></span>
<span data-ttu-id="18393-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="18393-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="18393-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18393-130">-Confirm</span></span>
<span data-ttu-id="18393-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18393-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18393-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18393-132">-WhatIf</span></span>
<span data-ttu-id="18393-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="18393-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18393-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18393-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18393-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18393-135">CommonParameters</span></span>
<span data-ttu-id="18393-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18393-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18393-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18393-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18393-138">입력</span><span class="sxs-lookup"><span data-stu-id="18393-138">INPUTS</span></span>

### <span data-ttu-id="18393-139">System.String</span><span class="sxs-lookup"><span data-stu-id="18393-139">System.String</span></span>

### <span data-ttu-id="18393-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18393-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="18393-141">출력</span><span class="sxs-lookup"><span data-stu-id="18393-141">OUTPUTS</span></span>

### <span data-ttu-id="18393-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18393-142">System.Boolean</span></span>

## <span data-ttu-id="18393-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18393-143">NOTES</span></span>

## <span data-ttu-id="18393-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18393-144">RELATED LINKS</span></span>
