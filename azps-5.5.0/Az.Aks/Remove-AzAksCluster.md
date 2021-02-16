---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199836"
---
# <span data-ttu-id="f9ce6-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f9ce6-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="f9ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ce6-103">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f9ce6-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9ce6-104">SYNTAX</span></span>

### <span data-ttu-id="f9ce6-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9ce6-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ce6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ce6-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ce6-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ce6-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ce6-108">설명</span><span class="sxs-lookup"><span data-stu-id="f9ce6-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ce6-109">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f9ce6-110">예제</span><span class="sxs-lookup"><span data-stu-id="f9ce6-110">EXAMPLES</span></span>

### <span data-ttu-id="f9ce6-111">기존 관리되는 Kubernetes 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="f9ce6-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f9ce6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="f9ce6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9ce6-113">-AsJob</span></span>
<span data-ttu-id="f9ce6-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9ce6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9ce6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ce6-115">-DefaultProfile</span></span>
<span data-ttu-id="f9ce6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ce6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f9ce6-117">-Force</span></span>
<span data-ttu-id="f9ce6-118">프롬프트 없이 관리되는 Kubernetes 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="f9ce6-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="f9ce6-119">-Id</span><span class="sxs-lookup"><span data-stu-id="f9ce6-119">-Id</span></span>
<span data-ttu-id="f9ce6-120">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="f9ce6-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f9ce6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9ce6-121">-InputObject</span></span>
<span data-ttu-id="f9ce6-122">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f9ce6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f9ce6-123">-Name</span></span>
<span data-ttu-id="f9ce6-124">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="f9ce6-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f9ce6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9ce6-125">-PassThru</span></span>
<span data-ttu-id="f9ce6-126">성공적으로 지우면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="f9ce6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ce6-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9ce6-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f9ce6-128">Resource group name</span></span>

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

### <span data-ttu-id="f9ce6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9ce6-129">-Confirm</span></span>
<span data-ttu-id="f9ce6-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ce6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ce6-131">-WhatIf</span></span>
<span data-ttu-id="f9ce6-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f9ce6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ce6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ce6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ce6-134">CommonParameters</span></span>
<span data-ttu-id="f9ce6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ce6-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9ce6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ce6-137">입력</span><span class="sxs-lookup"><span data-stu-id="f9ce6-137">INPUTS</span></span>

### <span data-ttu-id="f9ce6-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f9ce6-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f9ce6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f9ce6-139">System.String</span></span>

## <span data-ttu-id="f9ce6-140">출력</span><span class="sxs-lookup"><span data-stu-id="f9ce6-140">OUTPUTS</span></span>

### <span data-ttu-id="f9ce6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9ce6-141">System.Boolean</span></span>

## <span data-ttu-id="f9ce6-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9ce6-142">NOTES</span></span>

## <span data-ttu-id="f9ce6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9ce6-143">RELATED LINKS</span></span>
