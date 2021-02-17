---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191484"
---
# <span data-ttu-id="17525-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="17525-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="17525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17525-102">SYNOPSIS</span></span>
<span data-ttu-id="17525-103">클러스터를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="17525-103">Get or list clusters</span></span>

## <span data-ttu-id="17525-104">구문</span><span class="sxs-lookup"><span data-stu-id="17525-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17525-105">설명</span><span class="sxs-lookup"><span data-stu-id="17525-105">DESCRIPTION</span></span>
<span data-ttu-id="17525-106">클러스터를 얻거나 나열하고, "-ClusterName"이 제공되지 않은 경우 리소스 그룹 아래에 클러스터를 나열하고, "-ClusterName" 및 "ResourceGroupName"이 제공되지 않은 경우 구독 아래에 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="17525-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="17525-107">예제</span><span class="sxs-lookup"><span data-stu-id="17525-107">EXAMPLES</span></span>

### <span data-ttu-id="17525-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="17525-108">Example 1</span></span>
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

<span data-ttu-id="17525-109">클러스터를 얻게</span><span class="sxs-lookup"><span data-stu-id="17525-109">Get cluster</span></span>

## <span data-ttu-id="17525-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17525-110">PARAMETERS</span></span>

### <span data-ttu-id="17525-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="17525-111">-ClusterName</span></span>
<span data-ttu-id="17525-112">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17525-112">The cluster name.</span></span>

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

### <span data-ttu-id="17525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17525-113">-DefaultProfile</span></span>
<span data-ttu-id="17525-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17525-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17525-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17525-115">-ResourceGroupName</span></span>
<span data-ttu-id="17525-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17525-116">The resource group name.</span></span>

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

### <span data-ttu-id="17525-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17525-117">CommonParameters</span></span>
<span data-ttu-id="17525-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17525-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17525-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17525-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17525-120">입력</span><span class="sxs-lookup"><span data-stu-id="17525-120">INPUTS</span></span>

### <span data-ttu-id="17525-121">System.String</span><span class="sxs-lookup"><span data-stu-id="17525-121">System.String</span></span>

## <span data-ttu-id="17525-122">출력</span><span class="sxs-lookup"><span data-stu-id="17525-122">OUTPUTS</span></span>

### <span data-ttu-id="17525-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="17525-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="17525-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17525-124">NOTES</span></span>

## <span data-ttu-id="17525-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17525-125">RELATED LINKS</span></span>
