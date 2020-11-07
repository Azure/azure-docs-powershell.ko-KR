---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: eda9032cde317f418132e28917f7543d60ea0bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703279"
---
# <span data-ttu-id="dfe64-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="dfe64-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="dfe64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe64-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe64-103">지정 된 클러스터의 작업자 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfe64-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfe64-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe64-106">**AzureRmHDInsightClusterSize** cmdlet은 지정 된 Azure HDInsight 클러스터의 작업자 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="dfe64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfe64-107">EXAMPLES</span></span>

### <span data-ttu-id="dfe64-108">예제 1: 지정 된 클러스터의 크기 설정</span><span class="sxs-lookup"><span data-stu-id="dfe64-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="dfe64-109">이 명령은-hadoop-001 이라는 클러스터의 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="dfe64-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfe64-110">PARAMETERS</span></span>

### <span data-ttu-id="dfe64-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfe64-111">-ClusterName</span></span>
<span data-ttu-id="dfe64-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe64-113">-DefaultProfile</span></span>
<span data-ttu-id="dfe64-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dfe64-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfe64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe64-115">-ResourceGroupName</span></span>
<span data-ttu-id="dfe64-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe64-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="dfe64-117">-TargetInstanceCount</span></span>
<span data-ttu-id="dfe64-118">클러스터에서 원하는 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe64-119">CommonParameters</span></span>
<span data-ttu-id="dfe64-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe64-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe64-122">입력</span><span class="sxs-lookup"><span data-stu-id="dfe64-122">INPUTS</span></span>

### <span data-ttu-id="dfe64-123">않아야</span><span class="sxs-lookup"><span data-stu-id="dfe64-123">None</span></span>
<span data-ttu-id="dfe64-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe64-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfe64-125">출력</span><span class="sxs-lookup"><span data-stu-id="dfe64-125">OUTPUTS</span></span>

### <span data-ttu-id="dfe64-126">Microsoft. Azure. 관리. 클러스터</span><span class="sxs-lookup"><span data-stu-id="dfe64-126">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="dfe64-127">상속자</span><span class="sxs-lookup"><span data-stu-id="dfe64-127">NOTES</span></span>

## <span data-ttu-id="dfe64-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfe64-128">RELATED LINKS</span></span>

