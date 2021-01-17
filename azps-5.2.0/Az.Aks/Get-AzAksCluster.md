---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342482"
---
# <span data-ttu-id="9ccc4-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="9ccc4-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="9ccc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccc4-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccc4-103">Kubernetes 관리되는 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="9ccc4-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ccc4-104">SYNTAX</span></span>

### <span data-ttu-id="9ccc4-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ccc4-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ccc4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ccc4-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccc4-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ccc4-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ccc4-108">설명</span><span class="sxs-lookup"><span data-stu-id="9ccc4-108">DESCRIPTION</span></span>
<span data-ttu-id="9ccc4-109">Kubernetes 관리되는 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="9ccc4-110">예제</span><span class="sxs-lookup"><span data-stu-id="9ccc4-110">EXAMPLES</span></span>

### <span data-ttu-id="9ccc4-111">모든 Kubernetes 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="9ccc4-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="9ccc4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ccc4-112">PARAMETERS</span></span>

### <span data-ttu-id="9ccc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccc4-113">-DefaultProfile</span></span>
<span data-ttu-id="9ccc4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ccc4-115">-Id</span><span class="sxs-lookup"><span data-stu-id="9ccc4-115">-Id</span></span>
<span data-ttu-id="9ccc4-116">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="9ccc4-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9ccc4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ccc4-117">-Name</span></span>
<span data-ttu-id="9ccc4-118">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="9ccc4-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9ccc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ccc4-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9ccc4-120">Resource group name</span></span>

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

### <span data-ttu-id="9ccc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccc4-121">CommonParameters</span></span>
<span data-ttu-id="9ccc4-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccc4-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccc4-124">입력</span><span class="sxs-lookup"><span data-stu-id="9ccc4-124">INPUTS</span></span>

### <span data-ttu-id="9ccc4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9ccc4-125">System.String</span></span>

## <span data-ttu-id="9ccc4-126">출력</span><span class="sxs-lookup"><span data-stu-id="9ccc4-126">OUTPUTS</span></span>

### <span data-ttu-id="9ccc4-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9ccc4-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9ccc4-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ccc4-128">NOTES</span></span>

## <span data-ttu-id="9ccc4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ccc4-129">RELATED LINKS</span></span>
