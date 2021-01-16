---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326745"
---
# <span data-ttu-id="a1255-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a1255-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="a1255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1255-102">SYNOPSIS</span></span>
<span data-ttu-id="a1255-103">현재 구독 또는 지정된 리소스 그룹과 연결된 모든 Azure HDInsight 클러스터를 가져온 후 나열하거나 특정 클러스터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="a1255-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1255-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1255-105">설명</span><span class="sxs-lookup"><span data-stu-id="a1255-105">DESCRIPTION</span></span>
<span data-ttu-id="a1255-106">**Get-AzHDInsightCluster** cmdlet은 현재 구독에 대한 Azure HDInsight 서비스 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="a1255-107">*ClusterName* 매개 변수를 사용하여 특정 클러스터에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="a1255-108">예제</span><span class="sxs-lookup"><span data-stu-id="a1255-108">EXAMPLES</span></span>

### <span data-ttu-id="a1255-109">예제 1: 모든 Azure HDInsight 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="a1255-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="a1255-110">이 명령은 모든 Azure HDInsight 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="a1255-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1255-111">PARAMETERS</span></span>

### <span data-ttu-id="a1255-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a1255-112">-ClusterName</span></span>
<span data-ttu-id="a1255-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a1255-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1255-114">-DefaultProfile</span></span>
<span data-ttu-id="a1255-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a1255-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1255-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1255-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1255-117">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a1255-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1255-118">CommonParameters</span></span>
<span data-ttu-id="a1255-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1255-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1255-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1255-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1255-121">입력</span><span class="sxs-lookup"><span data-stu-id="a1255-121">INPUTS</span></span>

### <span data-ttu-id="a1255-122">없음</span><span class="sxs-lookup"><span data-stu-id="a1255-122">None</span></span>

## <span data-ttu-id="a1255-123">출력</span><span class="sxs-lookup"><span data-stu-id="a1255-123">OUTPUTS</span></span>

### <span data-ttu-id="a1255-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a1255-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a1255-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a1255-125">NOTES</span></span>

## <span data-ttu-id="a1255-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1255-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1255-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a1255-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="a1255-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a1255-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


