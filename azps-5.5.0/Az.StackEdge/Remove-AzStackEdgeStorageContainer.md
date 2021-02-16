---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178273"
---
# <span data-ttu-id="0de2d-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0de2d-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0de2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de2d-102">SYNOPSIS</span></span>
<span data-ttu-id="0de2d-103">디바이스에서 Edge Storage 계정에 대한 스토리지 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="0de2d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0de2d-104">SYNTAX</span></span>

### <span data-ttu-id="0de2d-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0de2d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de2d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de2d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de2d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de2d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de2d-108">설명</span><span class="sxs-lookup"><span data-stu-id="0de2d-108">DESCRIPTION</span></span>
<span data-ttu-id="0de2d-109">**Remove-AzStackEdgeStorageContainer** cmdlet은 Stack Edge 디바이스의 Edge Storage 계정에 대한 연결된 스토리지 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="0de2d-110">매개 변수로 제거할 저장소 컨테이너의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="0de2d-111">예제</span><span class="sxs-lookup"><span data-stu-id="0de2d-111">EXAMPLES</span></span>

### <span data-ttu-id="0de2d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0de2d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="0de2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0de2d-113">PARAMETERS</span></span>

### <span data-ttu-id="0de2d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de2d-114">-AsJob</span></span>
<span data-ttu-id="0de2d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0de2d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0de2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de2d-116">-DefaultProfile</span></span>
<span data-ttu-id="0de2d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de2d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0de2d-118">-DeviceName</span></span>
<span data-ttu-id="0de2d-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="0de2d-119">Device Name</span></span>

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

### <span data-ttu-id="0de2d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0de2d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="0de2d-121">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="0de2d-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de2d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0de2d-122">-InputObject</span></span>
<span data-ttu-id="0de2d-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="0de2d-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0de2d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0de2d-124">-Name</span></span>
<span data-ttu-id="0de2d-125">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="0de2d-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de2d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0de2d-126">-PassThru</span></span>
<span data-ttu-id="0de2d-127">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-127">returns true if successful</span></span>

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

### <span data-ttu-id="0de2d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de2d-128">-ResourceGroupName</span></span>
<span data-ttu-id="0de2d-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0de2d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="0de2d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0de2d-130">-ResourceId</span></span>
<span data-ttu-id="0de2d-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0de2d-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0de2d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0de2d-132">-Confirm</span></span>
<span data-ttu-id="0de2d-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de2d-134">-WhatIf</span></span>
<span data-ttu-id="0de2d-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0de2d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0de2d-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de2d-137">CommonParameters</span></span>
<span data-ttu-id="0de2d-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0de2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de2d-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0de2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de2d-140">입력</span><span class="sxs-lookup"><span data-stu-id="0de2d-140">INPUTS</span></span>

### <span data-ttu-id="0de2d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0de2d-141">System.String</span></span>

### <span data-ttu-id="0de2d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0de2d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0de2d-143">출력</span><span class="sxs-lookup"><span data-stu-id="0de2d-143">OUTPUTS</span></span>

### <span data-ttu-id="0de2d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0de2d-144">System.Boolean</span></span>

## <span data-ttu-id="0de2d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0de2d-145">NOTES</span></span>

## <span data-ttu-id="0de2d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0de2d-146">RELATED LINKS</span></span>
