---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955643"
---
# <span data-ttu-id="6418e-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6418e-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="6418e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6418e-102">SYNOPSIS</span></span>
<span data-ttu-id="6418e-103">클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="6418e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6418e-104">SYNTAX</span></span>

### <span data-ttu-id="6418e-105">BySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="6418e-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6418e-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6418e-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6418e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6418e-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6418e-108">설명</span><span class="sxs-lookup"><span data-stu-id="6418e-108">DESCRIPTION</span></span>
<span data-ttu-id="6418e-109">**Get-AzServiceFabricCluster에서** 클러스터 리소스 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="6418e-110">예제</span><span class="sxs-lookup"><span data-stu-id="6418e-110">EXAMPLES</span></span>

### <span data-ttu-id="6418e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6418e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="6418e-112">이 명령은 클러스터 'myCluster'에 대한 클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="6418e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6418e-113">PARAMETERS</span></span>

### <span data-ttu-id="6418e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6418e-114">-DefaultProfile</span></span>
<span data-ttu-id="6418e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6418e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6418e-116">-Name</span></span>
<span data-ttu-id="6418e-117">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="6418e-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6418e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6418e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6418e-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6418e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6418e-120">CommonParameters</span></span>
<span data-ttu-id="6418e-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6418e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6418e-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6418e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6418e-123">입력</span><span class="sxs-lookup"><span data-stu-id="6418e-123">INPUTS</span></span>

### <span data-ttu-id="6418e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6418e-124">System.String</span></span>

## <span data-ttu-id="6418e-125">출력</span><span class="sxs-lookup"><span data-stu-id="6418e-125">OUTPUTS</span></span>

### <span data-ttu-id="6418e-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6418e-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6418e-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6418e-127">NOTES</span></span>

## <span data-ttu-id="6418e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6418e-128">RELATED LINKS</span></span>
