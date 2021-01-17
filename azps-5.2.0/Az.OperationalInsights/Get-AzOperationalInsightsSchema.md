---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343358"
---
# <span data-ttu-id="ca7c7-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="ca7c7-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="ca7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7c7-103">작업 영역과 연결된 스마를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="ca7c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca7c7-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca7c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ca7c7-106">**Get-AzOperationalInsightsSchema** cmdlet은 해당 리소스 그룹 내에서 지정된 작업 영역과 연결된 스마마를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="ca7c7-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca7c7-107">EXAMPLES</span></span>

### <span data-ttu-id="ca7c7-108">예제 1: 작업 영역의 스마마를 얻게</span><span class="sxs-lookup"><span data-stu-id="ca7c7-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ca7c7-109">이 명령은 작업 영역과 연결된 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="ca7c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca7c7-110">PARAMETERS</span></span>

### <span data-ttu-id="ca7c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7c7-111">-DefaultProfile</span></span>
<span data-ttu-id="ca7c7-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ca7c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca7c7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7c7-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca7c7-114">작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ca7c7-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca7c7-115">-WorkspaceName</span></span>
<span data-ttu-id="ca7c7-116">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="ca7c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7c7-117">CommonParameters</span></span>
<span data-ttu-id="ca7c7-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7c7-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca7c7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7c7-120">입력</span><span class="sxs-lookup"><span data-stu-id="ca7c7-120">INPUTS</span></span>

### <span data-ttu-id="ca7c7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ca7c7-121">System.String</span></span>

## <span data-ttu-id="ca7c7-122">출력</span><span class="sxs-lookup"><span data-stu-id="ca7c7-122">OUTPUTS</span></span>

### <span data-ttu-id="ca7c7-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="ca7c7-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="ca7c7-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca7c7-124">NOTES</span></span>

## <span data-ttu-id="ca7c7-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca7c7-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca7c7-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca7c7-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


