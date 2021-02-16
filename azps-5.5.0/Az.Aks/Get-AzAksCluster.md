---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199884"
---
# <span data-ttu-id="36bbd-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="36bbd-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="36bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="36bbd-103">Kubernetes 관리되는 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36bbd-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="36bbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="36bbd-104">SYNTAX</span></span>

### <span data-ttu-id="36bbd-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="36bbd-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36bbd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36bbd-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36bbd-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36bbd-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36bbd-108">설명</span><span class="sxs-lookup"><span data-stu-id="36bbd-108">DESCRIPTION</span></span>
<span data-ttu-id="36bbd-109">Kubernetes 관리되는 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36bbd-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="36bbd-110">예제</span><span class="sxs-lookup"><span data-stu-id="36bbd-110">EXAMPLES</span></span>

### <span data-ttu-id="36bbd-111">모든 Kubernetes 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="36bbd-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="36bbd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36bbd-112">PARAMETERS</span></span>

### <span data-ttu-id="36bbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bbd-113">-DefaultProfile</span></span>
<span data-ttu-id="36bbd-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36bbd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36bbd-115">-Id</span><span class="sxs-lookup"><span data-stu-id="36bbd-115">-Id</span></span>
<span data-ttu-id="36bbd-116">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="36bbd-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="36bbd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36bbd-117">-Name</span></span>
<span data-ttu-id="36bbd-118">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="36bbd-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="36bbd-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="36bbd-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bbd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bbd-121">CommonParameters</span></span>
<span data-ttu-id="36bbd-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36bbd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bbd-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36bbd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bbd-124">입력</span><span class="sxs-lookup"><span data-stu-id="36bbd-124">INPUTS</span></span>

### <span data-ttu-id="36bbd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="36bbd-125">System.String</span></span>

## <span data-ttu-id="36bbd-126">출력</span><span class="sxs-lookup"><span data-stu-id="36bbd-126">OUTPUTS</span></span>

### <span data-ttu-id="36bbd-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="36bbd-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="36bbd-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36bbd-128">NOTES</span></span>

## <span data-ttu-id="36bbd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36bbd-129">RELATED LINKS</span></span>