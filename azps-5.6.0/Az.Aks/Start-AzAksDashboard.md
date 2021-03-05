---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5202f4c86d1d83d6e337c61ee6fc0f72a2b031de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998279"
---
# <span data-ttu-id="14c89-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="14c89-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="14c89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c89-102">SYNOPSIS</span></span>
<span data-ttu-id="14c89-103">관리되는 클러스터의 대시보드에 Kubectl SSH 터널을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="14c89-104">구문</span><span class="sxs-lookup"><span data-stu-id="14c89-104">SYNTAX</span></span>

### <span data-ttu-id="14c89-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="14c89-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c89-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c89-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c89-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c89-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c89-108">설명</span><span class="sxs-lookup"><span data-stu-id="14c89-108">DESCRIPTION</span></span>
<span data-ttu-id="14c89-109">관리되는 클러스터의 대시보드에 Kubectl SSH 터널을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="14c89-110">SSH 터널은 Kubectl-Tunnel PowerShell 작업에서 설정되고 를 실행하여 찾을 수 `Get-Job` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="14c89-111">터널은 을 통해 액세스할 수 [http://127.0.0.1:8001](http://127.0.0.1:8001) 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="14c89-112">예제</span><span class="sxs-lookup"><span data-stu-id="14c89-112">EXAMPLES</span></span>

### <span data-ttu-id="14c89-113">SSH 터널을 시작하고 Kubernetes 대시보드에 브라우저 열기</span><span class="sxs-lookup"><span data-stu-id="14c89-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="14c89-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14c89-114">PARAMETERS</span></span>

### <span data-ttu-id="14c89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c89-115">-DefaultProfile</span></span>
<span data-ttu-id="14c89-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c89-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="14c89-117">-DisableBrowser</span></span>
<span data-ttu-id="14c89-118">kubectl 포트 전달을 설정한 후 브라우저를 열지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="14c89-119">-Id</span><span class="sxs-lookup"><span data-stu-id="14c89-119">-Id</span></span>
<span data-ttu-id="14c89-120">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="14c89-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="14c89-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14c89-121">-InputObject</span></span>
<span data-ttu-id="14c89-122">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c89-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="14c89-123">-ListenPort</span></span>
<span data-ttu-id="14c89-124">대시보드에 대한 수신 수신 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-124">The listening port for the dashboard.</span></span> <span data-ttu-id="14c89-125">기본값은 8003입니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c89-126">-Name</span><span class="sxs-lookup"><span data-stu-id="14c89-126">-Name</span></span>
<span data-ttu-id="14c89-127">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="14c89-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="14c89-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14c89-128">-PassThru</span></span>
<span data-ttu-id="14c89-129">Cmdlet은 전달된 경우 KubeTunnelJob을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="14c89-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c89-130">-ResourceGroupName</span></span>
<span data-ttu-id="14c89-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="14c89-131">Resource group name</span></span>

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

### <span data-ttu-id="14c89-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c89-132">CommonParameters</span></span>
<span data-ttu-id="14c89-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14c89-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c89-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14c89-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c89-135">입력</span><span class="sxs-lookup"><span data-stu-id="14c89-135">INPUTS</span></span>

### <span data-ttu-id="14c89-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="14c89-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="14c89-137">System.String</span><span class="sxs-lookup"><span data-stu-id="14c89-137">System.String</span></span>

## <span data-ttu-id="14c89-138">출력</span><span class="sxs-lookup"><span data-stu-id="14c89-138">OUTPUTS</span></span>

### <span data-ttu-id="14c89-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="14c89-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="14c89-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14c89-140">NOTES</span></span>

## <span data-ttu-id="14c89-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14c89-141">RELATED LINKS</span></span>
