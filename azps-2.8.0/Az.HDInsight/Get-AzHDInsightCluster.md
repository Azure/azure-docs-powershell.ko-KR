---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689832"
---
# <span data-ttu-id="79233-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="79233-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="79233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79233-102">SYNOPSIS</span></span>
<span data-ttu-id="79233-103">현재 구독 또는 지정 된 리소스 그룹과 연결 된 모든 Azure HDInsight 클러스터를 가져오고 나열 하거나 특정 클러스터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="79233-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79233-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79233-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79233-105">DESCRIPTION</span></span>
<span data-ttu-id="79233-106">**AzHDInsightCluster** cmdlet은 현재 구독에 대 한 Azure HDInsight 서비스 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="79233-107">특정 클러스터에 대 한 세부 정보를 가져오려면 *ClusterName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="79233-108">예제의</span><span class="sxs-lookup"><span data-stu-id="79233-108">EXAMPLES</span></span>

### <span data-ttu-id="79233-109">예제 1: 모든 Azure HDInsight 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="79233-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="79233-110">이 명령은 모든 Azure HDInsight 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="79233-111">변수</span><span class="sxs-lookup"><span data-stu-id="79233-111">PARAMETERS</span></span>

### <span data-ttu-id="79233-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79233-112">-ClusterName</span></span>
<span data-ttu-id="79233-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="79233-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79233-114">-DefaultProfile</span></span>
<span data-ttu-id="79233-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="79233-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79233-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79233-116">-ResourceGroupName</span></span>
<span data-ttu-id="79233-117">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="79233-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79233-118">CommonParameters</span></span>
<span data-ttu-id="79233-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79233-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79233-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79233-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79233-121">입력</span><span class="sxs-lookup"><span data-stu-id="79233-121">INPUTS</span></span>

### <span data-ttu-id="79233-122">않아야</span><span class="sxs-lookup"><span data-stu-id="79233-122">None</span></span>

## <span data-ttu-id="79233-123">출력</span><span class="sxs-lookup"><span data-stu-id="79233-123">OUTPUTS</span></span>

### <span data-ttu-id="79233-124">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="79233-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="79233-125">상속자</span><span class="sxs-lookup"><span data-stu-id="79233-125">NOTES</span></span>

## <span data-ttu-id="79233-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79233-126">RELATED LINKS</span></span>

[<span data-ttu-id="79233-127">제거-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="79233-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="79233-128">-AzHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="79233-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


