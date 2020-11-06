---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532264"
---
# <span data-ttu-id="bb1b4-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bb1b4-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="bb1b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1b4-103">현재 구독 또는 지정 된 리소스 그룹과 연결 된 모든 Azure HDInsight 클러스터를 가져오고 나열 하거나 특정 클러스터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb1b4-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb1b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb1b4-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1b4-106">**AzureRmHDInsightCluster** cmdlet은 현재 구독에 대 한 Azure HDInsight 서비스 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="bb1b4-107">특정 클러스터에 대 한 세부 정보를 가져오려면 *ClusterName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="bb1b4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bb1b4-108">EXAMPLES</span></span>

### <span data-ttu-id="bb1b4-109">예제 1: 모든 Azure HDInsight 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="bb1b4-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="bb1b4-110">이 명령은 모든 Azure HDInsight 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="bb1b4-111">변수</span><span class="sxs-lookup"><span data-stu-id="bb1b4-111">PARAMETERS</span></span>

### <span data-ttu-id="bb1b4-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bb1b4-112">-ClusterName</span></span>
<span data-ttu-id="bb1b4-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bb1b4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb1b4-114">-ResourceGroupName</span></span>
<span data-ttu-id="bb1b4-115">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb1b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1b4-116">-DefaultProfile</span></span>
<span data-ttu-id="bb1b4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1b4-118">CommonParameters</span></span>
<span data-ttu-id="bb1b4-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1b4-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1b4-121">입력</span><span class="sxs-lookup"><span data-stu-id="bb1b4-121">INPUTS</span></span>

## <span data-ttu-id="bb1b4-122">출력</span><span class="sxs-lookup"><span data-stu-id="bb1b4-122">OUTPUTS</span></span>

### <span data-ttu-id="bb1b4-123">AzureHDInsightCluster의 목록 ' 1 [Microsoft Azure. t e m.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="bb1b4-124">상속자</span><span class="sxs-lookup"><span data-stu-id="bb1b4-124">NOTES</span></span>

## <span data-ttu-id="bb1b4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb1b4-125">RELATED LINKS</span></span>

[<span data-ttu-id="bb1b4-126">제거-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bb1b4-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="bb1b4-127">-AzureRmHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="bb1b4-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


