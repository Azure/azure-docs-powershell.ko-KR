---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304082"
---
# <span data-ttu-id="84f14-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="84f14-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="84f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84f14-102">SYNOPSIS</span></span>
<span data-ttu-id="84f14-103">지정 된 클러스터의 작업자 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="84f14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84f14-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84f14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84f14-105">DESCRIPTION</span></span>
<span data-ttu-id="84f14-106">**AzHDInsightClusterSize** cmdlet은 지정 된 Azure HDInsight 클러스터의 작업자 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="84f14-107">예제의</span><span class="sxs-lookup"><span data-stu-id="84f14-107">EXAMPLES</span></span>

### <span data-ttu-id="84f14-108">예제 1: 지정 된 클러스터의 크기 설정</span><span class="sxs-lookup"><span data-stu-id="84f14-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="84f14-109">이 명령은-hadoop-001 이라는 클러스터의 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="84f14-110">변수</span><span class="sxs-lookup"><span data-stu-id="84f14-110">PARAMETERS</span></span>

### <span data-ttu-id="84f14-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="84f14-111">-ClusterName</span></span>
<span data-ttu-id="84f14-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84f14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f14-113">-DefaultProfile</span></span>
<span data-ttu-id="84f14-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="84f14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84f14-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f14-115">-ResourceGroupName</span></span>
<span data-ttu-id="84f14-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84f14-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="84f14-117">-TargetInstanceCount</span></span>
<span data-ttu-id="84f14-118">클러스터에서 원하는 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84f14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f14-119">CommonParameters</span></span>
<span data-ttu-id="84f14-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f14-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f14-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f14-122">입력</span><span class="sxs-lookup"><span data-stu-id="84f14-122">INPUTS</span></span>

### <span data-ttu-id="84f14-123">않아야</span><span class="sxs-lookup"><span data-stu-id="84f14-123">None</span></span>

## <span data-ttu-id="84f14-124">출력</span><span class="sxs-lookup"><span data-stu-id="84f14-124">OUTPUTS</span></span>

### <span data-ttu-id="84f14-125">Microsoft. Azure. 관리. 클러스터</span><span class="sxs-lookup"><span data-stu-id="84f14-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="84f14-126">상속자</span><span class="sxs-lookup"><span data-stu-id="84f14-126">NOTES</span></span>

## <span data-ttu-id="84f14-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84f14-127">RELATED LINKS</span></span>
