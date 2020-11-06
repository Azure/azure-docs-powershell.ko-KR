---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529230"
---
# <span data-ttu-id="6df6c-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="6df6c-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="6df6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df6c-102">SYNOPSIS</span></span>
<span data-ttu-id="6df6c-103">사용할 수 있는 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6df6c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6df6c-105">DESCRIPTION</span></span>
<span data-ttu-id="6df6c-106">**Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="6df6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6df6c-107">EXAMPLES</span></span>

### <span data-ttu-id="6df6c-108">예제 1: 인텔리전스 팩 가져오기</span><span class="sxs-lookup"><span data-stu-id="6df6c-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="6df6c-109">이 명령은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="6df6c-110">변수</span><span class="sxs-lookup"><span data-stu-id="6df6c-110">PARAMETERS</span></span>

### <span data-ttu-id="6df6c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df6c-111">-ResourceGroupName</span></span>
<span data-ttu-id="6df6c-112">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6c-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6df6c-113">-WorkspaceName</span></span>
<span data-ttu-id="6df6c-114">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-114">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df6c-115">-DefaultProfile</span></span>
<span data-ttu-id="6df6c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6df6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df6c-117">CommonParameters</span></span>
<span data-ttu-id="6df6c-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df6c-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df6c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df6c-120">입력</span><span class="sxs-lookup"><span data-stu-id="6df6c-120">INPUTS</span></span>

## <span data-ttu-id="6df6c-121">출력</span><span class="sxs-lookup"><span data-stu-id="6df6c-121">OUTPUTS</span></span>

### <span data-ttu-id="6df6c-122">OperationalInsights의 ' 1 [Microsoft Azure. PSIntelligencePack] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6df6c-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="6df6c-123">상속자</span><span class="sxs-lookup"><span data-stu-id="6df6c-123">NOTES</span></span>

## <span data-ttu-id="6df6c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6df6c-124">RELATED LINKS</span></span>

[<span data-ttu-id="6df6c-125">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6df6c-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


