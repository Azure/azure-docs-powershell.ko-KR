---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 74c5504196a96408d66f8d64391552ebbc4449c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689205"
---
# <span data-ttu-id="16194-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="16194-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="16194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16194-102">SYNOPSIS</span></span>
<span data-ttu-id="16194-103">관리 되는 클러스터의 대시보드로 Kubectl SSH 터널을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16194-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="16194-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16194-104">SYNTAX</span></span>

### <span data-ttu-id="16194-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="16194-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16194-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16194-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16194-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16194-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16194-108">설명은</span><span class="sxs-lookup"><span data-stu-id="16194-108">DESCRIPTION</span></span>
<span data-ttu-id="16194-109">관리 되는 클러스터의 대시보드로 Kubectl SSH 터널을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16194-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="16194-110">SSH 터널은 Kubectl-Tunnel 라는 PowerShell 작업에 설정 되어 있으며, 실행 하 여 찾을 수 있습니다 `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="16194-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="16194-111">터널은를 통해 액세스할 수 있어야 합니다 [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="16194-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="16194-112">예제의</span><span class="sxs-lookup"><span data-stu-id="16194-112">EXAMPLES</span></span>

### <span data-ttu-id="16194-113">SSH 터널을 시작 하 고 브라우저를 Kubernetes 대시보드로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="16194-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="16194-114">변수</span><span class="sxs-lookup"><span data-stu-id="16194-114">PARAMETERS</span></span>

### <span data-ttu-id="16194-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16194-115">-DefaultProfile</span></span>
<span data-ttu-id="16194-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16194-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16194-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="16194-117">-DisableBrowser</span></span>
<span data-ttu-id="16194-118">Kubectl 포트를 establising 후 브라우저를 열지 마세요.</span><span class="sxs-lookup"><span data-stu-id="16194-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="16194-119">-Id</span><span class="sxs-lookup"><span data-stu-id="16194-119">-Id</span></span>
<span data-ttu-id="16194-120">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="16194-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="16194-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16194-121">-InputObject</span></span>
<span data-ttu-id="16194-122">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16194-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="16194-123">-이름</span><span class="sxs-lookup"><span data-stu-id="16194-123">-Name</span></span>
<span data-ttu-id="16194-124">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="16194-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="16194-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16194-125">-PassThru</span></span>
<span data-ttu-id="16194-126">Cmdlet이 전달 된 경우 KubeTunnelJob를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16194-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="16194-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16194-127">-ResourceGroupName</span></span>
<span data-ttu-id="16194-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="16194-128">Resource group name</span></span>

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

### <span data-ttu-id="16194-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16194-129">CommonParameters</span></span>
<span data-ttu-id="16194-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16194-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16194-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16194-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16194-132">입력</span><span class="sxs-lookup"><span data-stu-id="16194-132">INPUTS</span></span>

### <span data-ttu-id="16194-133">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="16194-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="16194-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16194-134">System.String</span></span>

## <span data-ttu-id="16194-135">출력</span><span class="sxs-lookup"><span data-stu-id="16194-135">OUTPUTS</span></span>

### <span data-ttu-id="16194-136">Aks. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="16194-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="16194-137">상속자</span><span class="sxs-lookup"><span data-stu-id="16194-137">NOTES</span></span>

## <span data-ttu-id="16194-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16194-138">RELATED LINKS</span></span>
