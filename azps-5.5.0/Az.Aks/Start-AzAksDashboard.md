---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199833"
---
# <span data-ttu-id="35b79-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="35b79-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="35b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35b79-102">SYNOPSIS</span></span>
<span data-ttu-id="35b79-103">관리되는 클러스터의 대시보드에 대한 Kubectl SSH 터널을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="35b79-104">구문</span><span class="sxs-lookup"><span data-stu-id="35b79-104">SYNTAX</span></span>

### <span data-ttu-id="35b79-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="35b79-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35b79-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b79-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35b79-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b79-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b79-108">설명</span><span class="sxs-lookup"><span data-stu-id="35b79-108">DESCRIPTION</span></span>
<span data-ttu-id="35b79-109">관리되는 클러스터의 대시보드에 대한 Kubectl SSH 터널을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="35b79-110">SSH 터널은 SSH 터널이 Kubectl-Tunnel PowerShell 작업에서 설정되고 실행하여 찾을 수 `Get-Job` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="35b79-111">터널은 .를 통해 액세스할 수 [http://127.0.0.1:8001](http://127.0.0.1:8001) 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="35b79-112">예제</span><span class="sxs-lookup"><span data-stu-id="35b79-112">EXAMPLES</span></span>

### <span data-ttu-id="35b79-113">SSH 터널을 시작하고 Kubernetes 대시보드에 대한 브라우저 열기</span><span class="sxs-lookup"><span data-stu-id="35b79-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="35b79-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35b79-114">PARAMETERS</span></span>

### <span data-ttu-id="35b79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b79-115">-DefaultProfile</span></span>
<span data-ttu-id="35b79-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35b79-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="35b79-117">-DisableBrowser</span></span>
<span data-ttu-id="35b79-118">kubectl 포트 전달을 설정한 후 브라우저를 열지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="35b79-119">-Id</span><span class="sxs-lookup"><span data-stu-id="35b79-119">-Id</span></span>
<span data-ttu-id="35b79-120">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="35b79-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="35b79-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35b79-121">-InputObject</span></span>
<span data-ttu-id="35b79-122">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="35b79-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="35b79-123">-ListenPort</span></span>
<span data-ttu-id="35b79-124">대시보드에 대한 수신 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-124">The listening port for the dashboard.</span></span> <span data-ttu-id="35b79-125">기본값은 8003입니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="35b79-126">-Name</span><span class="sxs-lookup"><span data-stu-id="35b79-126">-Name</span></span>
<span data-ttu-id="35b79-127">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="35b79-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="35b79-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35b79-128">-PassThru</span></span>
<span data-ttu-id="35b79-129">Cmdlet은 전달된 경우 KubeTunnelJob을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="35b79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b79-130">-ResourceGroupName</span></span>
<span data-ttu-id="35b79-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="35b79-131">Resource group name</span></span>

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

### <span data-ttu-id="35b79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b79-132">CommonParameters</span></span>
<span data-ttu-id="35b79-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35b79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b79-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35b79-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b79-135">입력</span><span class="sxs-lookup"><span data-stu-id="35b79-135">INPUTS</span></span>

### <span data-ttu-id="35b79-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="35b79-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="35b79-137">System.String</span><span class="sxs-lookup"><span data-stu-id="35b79-137">System.String</span></span>

## <span data-ttu-id="35b79-138">출력</span><span class="sxs-lookup"><span data-stu-id="35b79-138">OUTPUTS</span></span>

### <span data-ttu-id="35b79-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="35b79-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="35b79-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35b79-140">NOTES</span></span>

## <span data-ttu-id="35b79-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35b79-141">RELATED LINKS</span></span>
