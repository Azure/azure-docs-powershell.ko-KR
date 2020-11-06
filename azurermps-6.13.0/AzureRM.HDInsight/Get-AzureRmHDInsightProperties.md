---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 198f0db3cab8b2e0f6e8f9b466ac3e0027e4638c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530309"
---
# <span data-ttu-id="988db-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="988db-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="988db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988db-102">SYNOPSIS</span></span>
<span data-ttu-id="988db-103">사용 가능한 위치 및 용량 등의 HDInsight 서비스에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="988db-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="988db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="988db-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="988db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="988db-105">DESCRIPTION</span></span>
<span data-ttu-id="988db-106">**AzureRmHDInsightProperties** cmdlet은 사용 가능한 위치 목록, HDInsight 클러스터 버전, 사용 가능한 계산 용량 등 Azure HDInsight와 관련 된 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="988db-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="988db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="988db-107">EXAMPLES</span></span>

### <span data-ttu-id="988db-108">예제 1: Azure HDInsight 클러스터의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="988db-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="988db-109">이 명령은 HDInsight 서비스에서 속성을 가져옵니다 (동부 US 2 위치).</span><span class="sxs-lookup"><span data-stu-id="988db-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="988db-110">변수</span><span class="sxs-lookup"><span data-stu-id="988db-110">PARAMETERS</span></span>

### <span data-ttu-id="988db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988db-111">-DefaultProfile</span></span>
<span data-ttu-id="988db-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="988db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="988db-113">-위치</span><span class="sxs-lookup"><span data-stu-id="988db-113">-Location</span></span>
<span data-ttu-id="988db-114">HDInsight 속성을 가져올 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="988db-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="988db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988db-115">CommonParameters</span></span>
<span data-ttu-id="988db-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="988db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988db-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988db-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988db-118">입력</span><span class="sxs-lookup"><span data-stu-id="988db-118">INPUTS</span></span>

### <span data-ttu-id="988db-119">않아야</span><span class="sxs-lookup"><span data-stu-id="988db-119">None</span></span>

## <span data-ttu-id="988db-120">출력</span><span class="sxs-lookup"><span data-stu-id="988db-120">OUTPUTS</span></span>

### <span data-ttu-id="988db-121">CapabilitiesResponse를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="988db-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="988db-122">상속자</span><span class="sxs-lookup"><span data-stu-id="988db-122">NOTES</span></span>

## <span data-ttu-id="988db-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="988db-123">RELATED LINKS</span></span>
