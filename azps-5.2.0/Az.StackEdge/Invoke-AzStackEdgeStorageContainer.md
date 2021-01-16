---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354254"
---
# <span data-ttu-id="4510d-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4510d-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="4510d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4510d-102">SYNOPSIS</span></span>
<span data-ttu-id="4510d-103">저장소 컨테이너에서 특정 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="4510d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4510d-104">SYNTAX</span></span>

### <span data-ttu-id="4510d-105">InvokeByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4510d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4510d-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4510d-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4510d-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4510d-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4510d-108">설명</span><span class="sxs-lookup"><span data-stu-id="4510d-108">DESCRIPTION</span></span>
<span data-ttu-id="4510d-109">**Invoke-AzStackEdgeStorageContainer** cmdlet은 Stack Edge 디바이스의 저장소 컨테이너에서 데이터를 새로 고치기 위한 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="4510d-110">예제</span><span class="sxs-lookup"><span data-stu-id="4510d-110">EXAMPLES</span></span>

### <span data-ttu-id="4510d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4510d-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="4510d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4510d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="4510d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4510d-113">PARAMETERS</span></span>

### <span data-ttu-id="4510d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4510d-114">-AsJob</span></span>
<span data-ttu-id="4510d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4510d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4510d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4510d-116">-DefaultProfile</span></span>
<span data-ttu-id="4510d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4510d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4510d-118">-DeviceName</span></span>
<span data-ttu-id="4510d-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="4510d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4510d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="4510d-121">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="4510d-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4510d-122">-InputObject</span></span>
<span data-ttu-id="4510d-123">기존 EdgeStorageAccount 개체 제공</span><span class="sxs-lookup"><span data-stu-id="4510d-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4510d-124">-Name</span></span>
<span data-ttu-id="4510d-125">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="4510d-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4510d-126">-PassThru</span></span>
<span data-ttu-id="4510d-127">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-127">returns true if successful</span></span>

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

### <span data-ttu-id="4510d-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="4510d-128">-RefreshData</span></span>
<span data-ttu-id="4510d-129">클라우드의 데이터를 사용하여 컨테이너 메타데이터 새로 고침</span><span class="sxs-lookup"><span data-stu-id="4510d-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="4510d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4510d-130">-ResourceGroupName</span></span>
<span data-ttu-id="4510d-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4510d-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4510d-132">-ResourceId</span></span>
<span data-ttu-id="4510d-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4510d-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4510d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4510d-134">-Confirm</span></span>
<span data-ttu-id="4510d-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4510d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4510d-136">-WhatIf</span></span>
<span data-ttu-id="4510d-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4510d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4510d-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4510d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4510d-139">CommonParameters</span></span>
<span data-ttu-id="4510d-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4510d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4510d-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4510d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4510d-142">입력</span><span class="sxs-lookup"><span data-stu-id="4510d-142">INPUTS</span></span>

### <span data-ttu-id="4510d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4510d-143">System.String</span></span>

### <span data-ttu-id="4510d-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4510d-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="4510d-145">출력</span><span class="sxs-lookup"><span data-stu-id="4510d-145">OUTPUTS</span></span>

### <span data-ttu-id="4510d-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4510d-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="4510d-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4510d-147">NOTES</span></span>

## <span data-ttu-id="4510d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4510d-148">RELATED LINKS</span></span>