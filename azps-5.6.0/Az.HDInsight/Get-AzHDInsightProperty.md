---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009088"
---
# <span data-ttu-id="10223-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="10223-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="10223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10223-102">SYNOPSIS</span></span>
<span data-ttu-id="10223-103">사용 가능한 위치 및 용량과 같은 HDInsight 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="10223-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="10223-104">구문</span><span class="sxs-lookup"><span data-stu-id="10223-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10223-105">설명</span><span class="sxs-lookup"><span data-stu-id="10223-105">DESCRIPTION</span></span>
<span data-ttu-id="10223-106">**Get-AzHDInsightProperty** cmdlet은 사용 가능한 위치, HDInsight 클러스터 버전 및 사용 가능한 계산 용량 목록과 같은 Azure HDInsight에 특정 속성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="10223-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="10223-107">예제</span><span class="sxs-lookup"><span data-stu-id="10223-107">EXAMPLES</span></span>

### <span data-ttu-id="10223-108">예제 1: Azure HDInsight 클러스터의 속성 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="10223-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="10223-109">이 명령은 미국 동부 2 위치에서 HDInsight 서비스에서 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="10223-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="10223-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="10223-110">PARAMETERS</span></span>

### <span data-ttu-id="10223-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10223-111">-DefaultProfile</span></span>
<span data-ttu-id="10223-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10223-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10223-113">-Location</span><span class="sxs-lookup"><span data-stu-id="10223-113">-Location</span></span>
<span data-ttu-id="10223-114">HDInsight 속성을 페치할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10223-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="10223-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10223-115">CommonParameters</span></span>
<span data-ttu-id="10223-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10223-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10223-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10223-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10223-118">입력</span><span class="sxs-lookup"><span data-stu-id="10223-118">INPUTS</span></span>

### <span data-ttu-id="10223-119">없음</span><span class="sxs-lookup"><span data-stu-id="10223-119">None</span></span>
## <span data-ttu-id="10223-120">출력</span><span class="sxs-lookup"><span data-stu-id="10223-120">OUTPUTS</span></span>

### <span data-ttu-id="10223-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="10223-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="10223-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10223-122">NOTES</span></span>

## <span data-ttu-id="10223-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10223-123">RELATED LINKS</span></span>
