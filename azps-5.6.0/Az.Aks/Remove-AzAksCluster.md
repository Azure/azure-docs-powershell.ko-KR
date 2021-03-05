---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963344"
---
# <span data-ttu-id="4101e-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="4101e-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="4101e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4101e-102">SYNOPSIS</span></span>
<span data-ttu-id="4101e-103">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="4101e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4101e-104">SYNTAX</span></span>

### <span data-ttu-id="4101e-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4101e-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4101e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4101e-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4101e-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4101e-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4101e-108">설명</span><span class="sxs-lookup"><span data-stu-id="4101e-108">DESCRIPTION</span></span>
<span data-ttu-id="4101e-109">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="4101e-110">예제</span><span class="sxs-lookup"><span data-stu-id="4101e-110">EXAMPLES</span></span>

### <span data-ttu-id="4101e-111">기존 관리되는 Kubernetes 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="4101e-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="4101e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4101e-112">PARAMETERS</span></span>

### <span data-ttu-id="4101e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4101e-113">-AsJob</span></span>
<span data-ttu-id="4101e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4101e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4101e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4101e-115">-DefaultProfile</span></span>
<span data-ttu-id="4101e-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4101e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4101e-117">-Force</span></span>
<span data-ttu-id="4101e-118">프롬프트 없이 관리되는 Kubernetes 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="4101e-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="4101e-119">-Id</span><span class="sxs-lookup"><span data-stu-id="4101e-119">-Id</span></span>
<span data-ttu-id="4101e-120">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="4101e-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4101e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4101e-121">-InputObject</span></span>
<span data-ttu-id="4101e-122">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4101e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4101e-123">-Name</span></span>
<span data-ttu-id="4101e-124">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="4101e-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4101e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4101e-125">-PassThru</span></span>
<span data-ttu-id="4101e-126">지우기 성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="4101e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4101e-127">-ResourceGroupName</span></span>
<span data-ttu-id="4101e-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4101e-128">Resource group name</span></span>

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

### <span data-ttu-id="4101e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4101e-129">-Confirm</span></span>
<span data-ttu-id="4101e-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4101e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4101e-131">-WhatIf</span></span>
<span data-ttu-id="4101e-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4101e-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4101e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4101e-134">CommonParameters</span></span>
<span data-ttu-id="4101e-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4101e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4101e-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4101e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4101e-137">입력</span><span class="sxs-lookup"><span data-stu-id="4101e-137">INPUTS</span></span>

### <span data-ttu-id="4101e-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="4101e-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="4101e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4101e-139">System.String</span></span>

## <span data-ttu-id="4101e-140">출력</span><span class="sxs-lookup"><span data-stu-id="4101e-140">OUTPUTS</span></span>

### <span data-ttu-id="4101e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4101e-141">System.Boolean</span></span>

## <span data-ttu-id="4101e-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4101e-142">NOTES</span></span>

## <span data-ttu-id="4101e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4101e-143">RELATED LINKS</span></span>
