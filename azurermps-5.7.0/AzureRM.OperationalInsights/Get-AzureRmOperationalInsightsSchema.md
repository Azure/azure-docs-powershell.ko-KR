---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 1e1e56a4cf0e31af3d64377df05b6057354dd534
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702362"
---
# <span data-ttu-id="52eab-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="52eab-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="52eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52eab-102">SYNOPSIS</span></span>
<span data-ttu-id="52eab-103">작업 영역과 연결 된 스키마를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52eab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52eab-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52eab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52eab-105">DESCRIPTION</span></span>
<span data-ttu-id="52eab-106">**AzureRmOperationalInsightsSchema** cmdlet은 해당 리소스 그룹 내의 지정 된 작업 영역과 연결 된 스키마를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="52eab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="52eab-107">EXAMPLES</span></span>

### <span data-ttu-id="52eab-108">예제 1: 작업 영역에 대 한 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="52eab-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="52eab-109">이 명령은 작업 영역과 연결 된 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="52eab-110">변수</span><span class="sxs-lookup"><span data-stu-id="52eab-110">PARAMETERS</span></span>

### <span data-ttu-id="52eab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52eab-111">-DefaultProfile</span></span>
<span data-ttu-id="52eab-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="52eab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52eab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52eab-113">-ResourceGroupName</span></span>
<span data-ttu-id="52eab-114">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="52eab-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52eab-115">-WorkspaceName</span></span>
<span data-ttu-id="52eab-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="52eab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52eab-117">CommonParameters</span></span>
<span data-ttu-id="52eab-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52eab-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52eab-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52eab-120">입력</span><span class="sxs-lookup"><span data-stu-id="52eab-120">INPUTS</span></span>

### <span data-ttu-id="52eab-121">않아야</span><span class="sxs-lookup"><span data-stu-id="52eab-121">None</span></span>
<span data-ttu-id="52eab-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52eab-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52eab-123">출력</span><span class="sxs-lookup"><span data-stu-id="52eab-123">OUTPUTS</span></span>

### <span data-ttu-id="52eab-124">OperationalInsights. PSSearchGetSchemaResponse 응답</span><span class="sxs-lookup"><span data-stu-id="52eab-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="52eab-125">상속자</span><span class="sxs-lookup"><span data-stu-id="52eab-125">NOTES</span></span>

## <span data-ttu-id="52eab-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52eab-126">RELATED LINKS</span></span>

[<span data-ttu-id="52eab-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52eab-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


