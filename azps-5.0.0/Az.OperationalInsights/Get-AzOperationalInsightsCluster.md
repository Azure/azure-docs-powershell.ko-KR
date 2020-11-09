---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311213"
---
# <span data-ttu-id="2e89e-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="2e89e-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="2e89e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e89e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e89e-103">클러스터 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="2e89e-103">Get or list clusters</span></span>

## <span data-ttu-id="2e89e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e89e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e89e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e89e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e89e-106">클러스터 가져오기 또는 나열, "-ClusterName"이 제공 되지 않은 경우 리소스 그룹 아래에 클러스터 나열, "-ClusterName" 및 "ResourceGroupName"가 제공 되지 않은 경우 구독 아래에 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="2e89e-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="2e89e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2e89e-107">EXAMPLES</span></span>

### <span data-ttu-id="2e89e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e89e-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="2e89e-109">클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="2e89e-109">Get cluster</span></span>

## <span data-ttu-id="2e89e-110">변수</span><span class="sxs-lookup"><span data-stu-id="2e89e-110">PARAMETERS</span></span>

### <span data-ttu-id="2e89e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e89e-111">-ClusterName</span></span>
<span data-ttu-id="2e89e-112">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e89e-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e89e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e89e-113">-DefaultProfile</span></span>
<span data-ttu-id="2e89e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e89e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e89e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e89e-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e89e-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e89e-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e89e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e89e-117">CommonParameters</span></span>
<span data-ttu-id="2e89e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e89e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e89e-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e89e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e89e-120">입력</span><span class="sxs-lookup"><span data-stu-id="2e89e-120">INPUTS</span></span>

### <span data-ttu-id="2e89e-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e89e-121">System.String</span></span>

## <span data-ttu-id="2e89e-122">출력</span><span class="sxs-lookup"><span data-stu-id="2e89e-122">OUTPUTS</span></span>

### <span data-ttu-id="2e89e-123">OperationalInsights 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="2e89e-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="2e89e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2e89e-124">NOTES</span></span>

## <span data-ttu-id="2e89e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e89e-125">RELATED LINKS</span></span>
