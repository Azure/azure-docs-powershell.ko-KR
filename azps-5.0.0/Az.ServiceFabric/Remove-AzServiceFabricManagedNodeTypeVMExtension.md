---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215858"
---
# <span data-ttu-id="d91a3-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d91a3-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="d91a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d91a3-103">노드 형식에서 vm 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="d91a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d91a3-104">SYNTAX</span></span>

### <span data-ttu-id="d91a3-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="d91a3-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d91a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d91a3-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d91a3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d91a3-107">DESCRIPTION</span></span>
<span data-ttu-id="d91a3-108">이름으로 노드 형식에서 vm 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="d91a3-109">[AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) 를 사용 하 여 vmextensions 속성을 확인 하 여 노드 형식에 대 한 현재 확장을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="d91a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d91a3-110">EXAMPLES</span></span>

### <span data-ttu-id="d91a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d91a3-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="d91a3-112">이름에 따라 노드 형식에서 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="d91a3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d91a3-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="d91a3-114">노드 형식에서 확장명을 파이프를 사용 하 여 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="d91a3-115">변수</span><span class="sxs-lookup"><span data-stu-id="d91a3-115">PARAMETERS</span></span>

### <span data-ttu-id="d91a3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d91a3-116">-AsJob</span></span>
<span data-ttu-id="d91a3-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d91a3-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d91a3-118">-ClusterName</span></span>
<span data-ttu-id="d91a3-119">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d91a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91a3-120">-DefaultProfile</span></span>
<span data-ttu-id="d91a3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d91a3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d91a3-122">-InputObject</span></span>
<span data-ttu-id="d91a3-123">노드 형식 리소스</span><span class="sxs-lookup"><span data-stu-id="d91a3-123">Node type resource</span></span>

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

### <span data-ttu-id="d91a3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d91a3-124">-Name</span></span>
<span data-ttu-id="d91a3-125">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-125">extension name.</span></span>

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

### <span data-ttu-id="d91a3-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="d91a3-126">-NodeTypeName</span></span>
<span data-ttu-id="d91a3-127">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="d91a3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d91a3-128">-PassThru</span></span>
<span data-ttu-id="d91a3-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="d91a3-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d91a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="d91a3-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d91a3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d91a3-132">-Confirm</span></span>
<span data-ttu-id="d91a3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91a3-134">-WhatIf</span></span>
<span data-ttu-id="d91a3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d91a3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91a3-137">CommonParameters</span></span>
<span data-ttu-id="d91a3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91a3-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d91a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91a3-140">입력</span><span class="sxs-lookup"><span data-stu-id="d91a3-140">INPUTS</span></span>

### <span data-ttu-id="d91a3-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d91a3-141">System.String</span></span>

## <span data-ttu-id="d91a3-142">출력</span><span class="sxs-lookup"><span data-stu-id="d91a3-142">OUTPUTS</span></span>

### <span data-ttu-id="d91a3-143">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="d91a3-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d91a3-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d91a3-144">NOTES</span></span>

## <span data-ttu-id="d91a3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d91a3-145">RELATED LINKS</span></span>
