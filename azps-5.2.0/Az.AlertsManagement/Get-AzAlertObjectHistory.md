---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343485"
---
# <span data-ttu-id="aea28-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="aea28-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="aea28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea28-102">SYNOPSIS</span></span>
<span data-ttu-id="aea28-103">경고 기록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-103">Gets Alert History information</span></span>

## <span data-ttu-id="aea28-104">구문</span><span class="sxs-lookup"><span data-stu-id="aea28-104">SYNTAX</span></span>

### <span data-ttu-id="aea28-105">ByAlertId(기본값)</span><span class="sxs-lookup"><span data-stu-id="aea28-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aea28-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea28-107">설명</span><span class="sxs-lookup"><span data-stu-id="aea28-107">DESCRIPTION</span></span>
<span data-ttu-id="aea28-108">**Get-AzAlertObjectHistory** cmdlet은 경고 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="aea28-109">예제</span><span class="sxs-lookup"><span data-stu-id="aea28-109">EXAMPLES</span></span>

### <span data-ttu-id="aea28-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="aea28-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="aea28-111">경고 기록 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-111">Gets alert history details.</span></span> 

## <span data-ttu-id="aea28-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aea28-112">PARAMETERS</span></span>

### <span data-ttu-id="aea28-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="aea28-113">-AlertId</span></span>
<span data-ttu-id="aea28-114">경고의 고유 식별자/경고의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea28-115">-DefaultProfile</span></span>
<span data-ttu-id="aea28-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aea28-117">-InputObject</span></span>
<span data-ttu-id="aea28-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aea28-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea28-119">CommonParameters</span></span>
<span data-ttu-id="aea28-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aea28-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea28-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aea28-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea28-122">입력</span><span class="sxs-lookup"><span data-stu-id="aea28-122">INPUTS</span></span>

### <span data-ttu-id="aea28-123">없음</span><span class="sxs-lookup"><span data-stu-id="aea28-123">None</span></span>

## <span data-ttu-id="aea28-124">출력</span><span class="sxs-lookup"><span data-stu-id="aea28-124">OUTPUTS</span></span>

### <span data-ttu-id="aea28-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="aea28-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="aea28-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aea28-126">NOTES</span></span>

## <span data-ttu-id="aea28-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aea28-127">RELATED LINKS</span></span>
