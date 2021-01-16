---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341925"
---
# <span data-ttu-id="db05b-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="db05b-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="db05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db05b-102">SYNOPSIS</span></span>
<span data-ttu-id="db05b-103">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="db05b-104">구문</span><span class="sxs-lookup"><span data-stu-id="db05b-104">SYNTAX</span></span>

### <span data-ttu-id="db05b-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="db05b-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db05b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db05b-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db05b-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db05b-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db05b-108">설명</span><span class="sxs-lookup"><span data-stu-id="db05b-108">DESCRIPTION</span></span>
<span data-ttu-id="db05b-109">관리되는 Kubernetes 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="db05b-110">예제</span><span class="sxs-lookup"><span data-stu-id="db05b-110">EXAMPLES</span></span>

### <span data-ttu-id="db05b-111">기존 관리되는 Kubernetes 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="db05b-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="db05b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db05b-112">PARAMETERS</span></span>

### <span data-ttu-id="db05b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db05b-113">-AsJob</span></span>
<span data-ttu-id="db05b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="db05b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db05b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db05b-115">-DefaultProfile</span></span>
<span data-ttu-id="db05b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db05b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db05b-117">-Force</span></span>
<span data-ttu-id="db05b-118">프롬프트 없이 관리되는 Kubernetes 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="db05b-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="db05b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="db05b-119">-Id</span></span>
<span data-ttu-id="db05b-120">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="db05b-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="db05b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db05b-121">-InputObject</span></span>
<span data-ttu-id="db05b-122">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="db05b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="db05b-123">-Name</span></span>
<span data-ttu-id="db05b-124">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="db05b-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="db05b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db05b-125">-PassThru</span></span>
<span data-ttu-id="db05b-126">성공적으로 지우면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="db05b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db05b-127">-ResourceGroupName</span></span>
<span data-ttu-id="db05b-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="db05b-128">Resource group name</span></span>

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

### <span data-ttu-id="db05b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db05b-129">-Confirm</span></span>
<span data-ttu-id="db05b-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db05b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db05b-131">-WhatIf</span></span>
<span data-ttu-id="db05b-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="db05b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db05b-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db05b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db05b-134">CommonParameters</span></span>
<span data-ttu-id="db05b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db05b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db05b-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db05b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db05b-137">입력</span><span class="sxs-lookup"><span data-stu-id="db05b-137">INPUTS</span></span>

### <span data-ttu-id="db05b-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="db05b-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="db05b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="db05b-139">System.String</span></span>

## <span data-ttu-id="db05b-140">출력</span><span class="sxs-lookup"><span data-stu-id="db05b-140">OUTPUTS</span></span>

### <span data-ttu-id="db05b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db05b-141">System.Boolean</span></span>

## <span data-ttu-id="db05b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db05b-142">NOTES</span></span>

## <span data-ttu-id="db05b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db05b-143">RELATED LINKS</span></span>
