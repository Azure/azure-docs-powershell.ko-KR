---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214735"
---
# <span data-ttu-id="750aa-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="750aa-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="750aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="750aa-102">SYNOPSIS</span></span>
<span data-ttu-id="750aa-103">작업 영역과 연결 된 스키마를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="750aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="750aa-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="750aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="750aa-105">DESCRIPTION</span></span>
<span data-ttu-id="750aa-106">**AzOperationalInsightsSchema** cmdlet은 해당 리소스 그룹 내의 지정 된 작업 영역과 연결 된 스키마를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="750aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="750aa-107">EXAMPLES</span></span>

### <span data-ttu-id="750aa-108">예제 1: 작업 영역에 대 한 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="750aa-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="750aa-109">이 명령은 작업 영역과 연결 된 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="750aa-110">변수</span><span class="sxs-lookup"><span data-stu-id="750aa-110">PARAMETERS</span></span>

### <span data-ttu-id="750aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750aa-111">-DefaultProfile</span></span>
<span data-ttu-id="750aa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="750aa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="750aa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="750aa-113">-ResourceGroupName</span></span>
<span data-ttu-id="750aa-114">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="750aa-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="750aa-115">-WorkspaceName</span></span>
<span data-ttu-id="750aa-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="750aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750aa-117">CommonParameters</span></span>
<span data-ttu-id="750aa-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="750aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750aa-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="750aa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750aa-120">입력</span><span class="sxs-lookup"><span data-stu-id="750aa-120">INPUTS</span></span>

### <span data-ttu-id="750aa-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="750aa-121">System.String</span></span>

## <span data-ttu-id="750aa-122">출력</span><span class="sxs-lookup"><span data-stu-id="750aa-122">OUTPUTS</span></span>

### <span data-ttu-id="750aa-123">OperationalInsights. PSSearchGetSchemaResponse 응답</span><span class="sxs-lookup"><span data-stu-id="750aa-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="750aa-124">상속자</span><span class="sxs-lookup"><span data-stu-id="750aa-124">NOTES</span></span>

## <span data-ttu-id="750aa-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="750aa-125">RELATED LINKS</span></span>

[<span data-ttu-id="750aa-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="750aa-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


