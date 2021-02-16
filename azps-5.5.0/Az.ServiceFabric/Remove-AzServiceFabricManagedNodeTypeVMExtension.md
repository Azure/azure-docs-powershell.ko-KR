---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183457"
---
# <span data-ttu-id="9366a-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="9366a-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="9366a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9366a-102">SYNOPSIS</span></span>
<span data-ttu-id="9366a-103">노드 형식에서 vm 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="9366a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9366a-104">SYNTAX</span></span>

### <span data-ttu-id="9366a-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="9366a-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9366a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9366a-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9366a-107">설명</span><span class="sxs-lookup"><span data-stu-id="9366a-107">DESCRIPTION</span></span>
<span data-ttu-id="9366a-108">이름별로 노드 형식에서 vm 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="9366a-109">[Get-AzServiceFabricManagedNodeType을](./Get-AzServiceFabricManagedNodeType.md) 사용하여 VmExtensions 속성을 확인하여 노드 형식에서 현재 확장을 봐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="9366a-110">예제</span><span class="sxs-lookup"><span data-stu-id="9366a-110">EXAMPLES</span></span>

### <span data-ttu-id="9366a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9366a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="9366a-112">노드 형식에서 이름별로 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="9366a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9366a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="9366a-114">파이핑을 사용하여 이름별로 노드 형식에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="9366a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9366a-115">PARAMETERS</span></span>

### <span data-ttu-id="9366a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9366a-116">-AsJob</span></span>
<span data-ttu-id="9366a-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9366a-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9366a-118">-ClusterName</span></span>
<span data-ttu-id="9366a-119">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9366a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9366a-120">-DefaultProfile</span></span>
<span data-ttu-id="9366a-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9366a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9366a-122">-InputObject</span></span>
<span data-ttu-id="9366a-123">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="9366a-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9366a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9366a-124">-Name</span></span>
<span data-ttu-id="9366a-125">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9366a-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="9366a-126">-NodeTypeName</span></span>
<span data-ttu-id="9366a-127">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9366a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9366a-128">-PassThru</span></span>
<span data-ttu-id="9366a-129">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="9366a-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9366a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9366a-130">-ResourceGroupName</span></span>
<span data-ttu-id="9366a-131">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9366a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9366a-132">-Confirm</span></span>
<span data-ttu-id="9366a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9366a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9366a-134">-WhatIf</span></span>
<span data-ttu-id="9366a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9366a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9366a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9366a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9366a-137">CommonParameters</span></span>
<span data-ttu-id="9366a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9366a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9366a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9366a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9366a-140">입력</span><span class="sxs-lookup"><span data-stu-id="9366a-140">INPUTS</span></span>

### <span data-ttu-id="9366a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9366a-141">System.String</span></span>

## <span data-ttu-id="9366a-142">출력</span><span class="sxs-lookup"><span data-stu-id="9366a-142">OUTPUTS</span></span>

### <span data-ttu-id="9366a-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="9366a-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="9366a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9366a-144">NOTES</span></span>

## <span data-ttu-id="9366a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9366a-145">RELATED LINKS</span></span>
