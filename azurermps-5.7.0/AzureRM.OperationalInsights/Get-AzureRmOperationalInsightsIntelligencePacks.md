---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528894"
---
# <span data-ttu-id="cb932-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="cb932-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="cb932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb932-102">SYNOPSIS</span></span>
<span data-ttu-id="cb932-103">사용할 수 있는 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb932-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb932-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb932-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb932-105">DESCRIPTION</span></span>
<span data-ttu-id="cb932-106">**Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="cb932-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cb932-107">EXAMPLES</span></span>

### <span data-ttu-id="cb932-108">예제 1: 인텔리전스 팩 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb932-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="cb932-109">이 명령은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="cb932-110">변수</span><span class="sxs-lookup"><span data-stu-id="cb932-110">PARAMETERS</span></span>

### <span data-ttu-id="cb932-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb932-111">-DefaultProfile</span></span>
<span data-ttu-id="cb932-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cb932-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb932-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb932-113">-ResourceGroupName</span></span>
<span data-ttu-id="cb932-114">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb932-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb932-115">-WorkspaceName</span></span>
<span data-ttu-id="cb932-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb932-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb932-117">CommonParameters</span></span>
<span data-ttu-id="cb932-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb932-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb932-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb932-120">입력</span><span class="sxs-lookup"><span data-stu-id="cb932-120">INPUTS</span></span>

### <span data-ttu-id="cb932-121">않아야</span><span class="sxs-lookup"><span data-stu-id="cb932-121">None</span></span>
<span data-ttu-id="cb932-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb932-123">출력</span><span class="sxs-lookup"><span data-stu-id="cb932-123">OUTPUTS</span></span>

### <span data-ttu-id="cb932-124">OperationalInsights의 ' 1 [Microsoft Azure. PSIntelligencePack] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cb932-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="cb932-125">상속자</span><span class="sxs-lookup"><span data-stu-id="cb932-125">NOTES</span></span>

## <span data-ttu-id="cb932-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb932-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb932-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb932-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


