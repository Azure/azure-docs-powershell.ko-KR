---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: ff789a04be2a6f448d4850891f368cbb7ca91c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879802"
---
# <span data-ttu-id="179d1-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="179d1-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="179d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179d1-102">SYNOPSIS</span></span>
<span data-ttu-id="179d1-103">현재 구독 또는 지정 된 리소스 그룹과 연결 된 모든 Azure HDInsight 클러스터를 가져오고 나열 하거나 특정 클러스터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="179d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="179d1-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="179d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="179d1-105">DESCRIPTION</span></span>
<span data-ttu-id="179d1-106">**AzHDInsightCluster** cmdlet은 현재 구독에 대 한 Azure HDInsight 서비스 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="179d1-107">특정 클러스터에 대 한 세부 정보를 가져오려면 *ClusterName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="179d1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="179d1-108">EXAMPLES</span></span>

### <span data-ttu-id="179d1-109">예제 1: 모든 Azure HDInsight 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="179d1-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="179d1-110">이 명령은 모든 Azure HDInsight 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="179d1-111">변수</span><span class="sxs-lookup"><span data-stu-id="179d1-111">PARAMETERS</span></span>

### <span data-ttu-id="179d1-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="179d1-112">-ClusterName</span></span>
<span data-ttu-id="179d1-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179d1-114">-DefaultProfile</span></span>
<span data-ttu-id="179d1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="179d1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="179d1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="179d1-116">-ResourceGroupName</span></span>
<span data-ttu-id="179d1-117">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179d1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179d1-118">CommonParameters</span></span>
<span data-ttu-id="179d1-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="179d1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179d1-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179d1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179d1-121">입력</span><span class="sxs-lookup"><span data-stu-id="179d1-121">INPUTS</span></span>

### <span data-ttu-id="179d1-122">않아야</span><span class="sxs-lookup"><span data-stu-id="179d1-122">None</span></span>

## <span data-ttu-id="179d1-123">출력</span><span class="sxs-lookup"><span data-stu-id="179d1-123">OUTPUTS</span></span>

### <span data-ttu-id="179d1-124">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="179d1-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="179d1-125">상속자</span><span class="sxs-lookup"><span data-stu-id="179d1-125">NOTES</span></span>

## <span data-ttu-id="179d1-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="179d1-126">RELATED LINKS</span></span>

[<span data-ttu-id="179d1-127">제거-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="179d1-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="179d1-128">-AzHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="179d1-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


