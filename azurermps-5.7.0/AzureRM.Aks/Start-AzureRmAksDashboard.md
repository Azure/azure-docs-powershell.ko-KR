---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703296"
---
# <span data-ttu-id="8a234-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="8a234-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="8a234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a234-102">SYNOPSIS</span></span>
<span data-ttu-id="8a234-103">관리 되는 클러스터의 대시보드로 Kubectl SSH 터널을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a234-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a234-104">SYNTAX</span></span>

### <span data-ttu-id="8a234-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a234-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a234-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a234-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a234-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a234-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a234-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8a234-108">DESCRIPTION</span></span>
<span data-ttu-id="8a234-109">관리 되는 클러스터의 대시보드로 Kubectl SSH 터널을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="8a234-110">SSH 터널은 Kubectl-Tunnel 라는 PowerShell 작업에 설정 되어 있으며, 실행 하 여 찾을 수 있습니다 `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="8a234-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="8a234-111">터널은를 통해 액세스할 수 있어야 합니다 [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="8a234-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="8a234-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8a234-112">EXAMPLES</span></span>

### <span data-ttu-id="8a234-113">SSH 터널을 시작 하 고 브라우저를 Kubernetes 대시보드로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="8a234-114">변수</span><span class="sxs-lookup"><span data-stu-id="8a234-114">PARAMETERS</span></span>

### <span data-ttu-id="8a234-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a234-115">-DefaultProfile</span></span>
<span data-ttu-id="8a234-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="8a234-117">-DisableBrowser</span></span>
<span data-ttu-id="8a234-118">Kubectl 포트를 establising 후 브라우저를 열지 마세요.</span><span class="sxs-lookup"><span data-stu-id="8a234-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-119">-Id</span><span class="sxs-lookup"><span data-stu-id="8a234-119">-Id</span></span>
<span data-ttu-id="8a234-120">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a234-121">-InputObject</span></span>
<span data-ttu-id="8a234-122">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8a234-123">-Name</span></span>
<span data-ttu-id="8a234-124">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="8a234-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a234-125">-PassThru</span></span>
<span data-ttu-id="8a234-126">Cmdlet이 전달 된 경우 KubeTunnelJob를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a234-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a234-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8a234-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a234-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a234-129">CommonParameters</span></span>
<span data-ttu-id="8a234-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a234-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a234-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a234-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a234-132">입력</span><span class="sxs-lookup"><span data-stu-id="8a234-132">INPUTS</span></span>

### <span data-ttu-id="8a234-133">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="8a234-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="8a234-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a234-134">System.String</span></span>

## <span data-ttu-id="8a234-135">출력</span><span class="sxs-lookup"><span data-stu-id="8a234-135">OUTPUTS</span></span>

### <span data-ttu-id="8a234-136">Aks. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="8a234-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="8a234-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8a234-137">NOTES</span></span>

## <span data-ttu-id="8a234-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a234-138">RELATED LINKS</span></span>
