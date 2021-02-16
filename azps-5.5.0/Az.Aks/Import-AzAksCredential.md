---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199857"
---
# <span data-ttu-id="c720d-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="c720d-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="c720d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c720d-102">SYNOPSIS</span></span>
<span data-ttu-id="c720d-103">관리되는 Kubernetes 클러스터에 대한 Kubectl 구성을 가져오고 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c720d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c720d-104">SYNTAX</span></span>

### <span data-ttu-id="c720d-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c720d-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c720d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c720d-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c720d-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c720d-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c720d-108">설명</span><span class="sxs-lookup"><span data-stu-id="c720d-108">DESCRIPTION</span></span>
<span data-ttu-id="c720d-109">관리되는 Kubernetes 클러스터에 대한 Kubectl 구성을 가져오고 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c720d-110">예제</span><span class="sxs-lookup"><span data-stu-id="c720d-110">EXAMPLES</span></span>

### <span data-ttu-id="c720d-111">Kubectl 구성 가져오기 및 병합</span><span class="sxs-lookup"><span data-stu-id="c720d-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c720d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c720d-112">PARAMETERS</span></span>

### <span data-ttu-id="c720d-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="c720d-113">-Admin</span></span>
<span data-ttu-id="c720d-114">기본 'clusterUser' 대신 'clusterAdmin' kubectl 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="c720d-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="c720d-115">-ConfigPath</span></span>
<span data-ttu-id="c720d-116">만들거나 업데이트할 kubectl 구성 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="c720d-117">대신 '-'를 사용하여 stdout에 YAML을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="c720d-118">기본값: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="c720d-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c720d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c720d-119">-DefaultProfile</span></span>
<span data-ttu-id="c720d-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c720d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c720d-121">-Force</span></span>
<span data-ttu-id="c720d-122">기본값인 경우에도 Kubernetes 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="c720d-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="c720d-123">-Id</span><span class="sxs-lookup"><span data-stu-id="c720d-123">-Id</span></span>
<span data-ttu-id="c720d-124">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="c720d-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c720d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c720d-125">-InputObject</span></span>
<span data-ttu-id="c720d-126">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c720d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c720d-127">-Name</span></span>
<span data-ttu-id="c720d-128">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="c720d-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c720d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c720d-129">-PassThru</span></span>
<span data-ttu-id="c720d-130">가져오기에 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="c720d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c720d-131">-ResourceGroupName</span></span>
<span data-ttu-id="c720d-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c720d-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c720d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c720d-133">-Confirm</span></span>
<span data-ttu-id="c720d-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c720d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c720d-135">-WhatIf</span></span>
<span data-ttu-id="c720d-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c720d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c720d-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c720d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c720d-138">CommonParameters</span></span>
<span data-ttu-id="c720d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c720d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c720d-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c720d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c720d-141">입력</span><span class="sxs-lookup"><span data-stu-id="c720d-141">INPUTS</span></span>

### <span data-ttu-id="c720d-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c720d-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c720d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c720d-143">System.String</span></span>

## <span data-ttu-id="c720d-144">출력</span><span class="sxs-lookup"><span data-stu-id="c720d-144">OUTPUTS</span></span>

### <span data-ttu-id="c720d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c720d-145">System.String</span></span>

## <span data-ttu-id="c720d-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c720d-146">NOTES</span></span>

## <span data-ttu-id="c720d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c720d-147">RELATED LINKS</span></span>
