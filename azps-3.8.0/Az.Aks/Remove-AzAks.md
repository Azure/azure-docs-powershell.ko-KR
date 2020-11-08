---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: 25a138b326a2fc086138f25a3d85f5182ba027fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034682"
---
# <span data-ttu-id="71859-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="71859-101">Remove-AzAks</span></span>

## <span data-ttu-id="71859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71859-102">SYNOPSIS</span></span>
<span data-ttu-id="71859-103">관리 Kubernetes 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71859-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="71859-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71859-104">SYNTAX</span></span>

### <span data-ttu-id="71859-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="71859-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71859-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71859-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71859-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71859-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71859-108">설명은</span><span class="sxs-lookup"><span data-stu-id="71859-108">DESCRIPTION</span></span>
<span data-ttu-id="71859-109">관리 Kubernetes 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71859-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="71859-110">예제의</span><span class="sxs-lookup"><span data-stu-id="71859-110">EXAMPLES</span></span>

### <span data-ttu-id="71859-111">기존 관리 Kubernetes 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="71859-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="71859-112">변수</span><span class="sxs-lookup"><span data-stu-id="71859-112">PARAMETERS</span></span>

### <span data-ttu-id="71859-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71859-113">-AsJob</span></span>
<span data-ttu-id="71859-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="71859-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71859-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71859-115">-DefaultProfile</span></span>
<span data-ttu-id="71859-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71859-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71859-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71859-117">-Force</span></span>
<span data-ttu-id="71859-118">메시지를 표시 하지 않고 관리 Kubernetes 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="71859-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="71859-119">-Id</span><span class="sxs-lookup"><span data-stu-id="71859-119">-Id</span></span>
<span data-ttu-id="71859-120">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="71859-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="71859-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71859-121">-InputObject</span></span>
<span data-ttu-id="71859-122">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71859-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="71859-123">-이름</span><span class="sxs-lookup"><span data-stu-id="71859-123">-Name</span></span>
<span data-ttu-id="71859-124">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="71859-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="71859-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71859-125">-PassThru</span></span>
<span data-ttu-id="71859-126">삭제에 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71859-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="71859-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71859-127">-ResourceGroupName</span></span>
<span data-ttu-id="71859-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="71859-128">Resource group name</span></span>

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

### <span data-ttu-id="71859-129">-확인</span><span class="sxs-lookup"><span data-stu-id="71859-129">-Confirm</span></span>
<span data-ttu-id="71859-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71859-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71859-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71859-131">-WhatIf</span></span>
<span data-ttu-id="71859-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71859-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71859-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71859-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71859-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71859-134">CommonParameters</span></span>
<span data-ttu-id="71859-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71859-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71859-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71859-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71859-137">입력</span><span class="sxs-lookup"><span data-stu-id="71859-137">INPUTS</span></span>

### <span data-ttu-id="71859-138">Aks. p U<c13> Netescluster</span><span class="sxs-lookup"><span data-stu-id="71859-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="71859-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="71859-139">System.String</span></span>

## <span data-ttu-id="71859-140">출력</span><span class="sxs-lookup"><span data-stu-id="71859-140">OUTPUTS</span></span>

### <span data-ttu-id="71859-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="71859-141">System.Boolean</span></span>

## <span data-ttu-id="71859-142">상속자</span><span class="sxs-lookup"><span data-stu-id="71859-142">NOTES</span></span>

## <span data-ttu-id="71859-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71859-143">RELATED LINKS</span></span>
