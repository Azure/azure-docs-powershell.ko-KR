---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 31b72f68151132fc4dca1bddd18c1a15b6a36f3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961019"
---
# <span data-ttu-id="058b7-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="058b7-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="058b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="058b7-102">SYNOPSIS</span></span>
<span data-ttu-id="058b7-103">경고 기록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-103">Gets Alert History information</span></span>

## <span data-ttu-id="058b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="058b7-104">SYNTAX</span></span>

### <span data-ttu-id="058b7-105">ByAlertId(기본값)</span><span class="sxs-lookup"><span data-stu-id="058b7-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="058b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="058b7-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="058b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="058b7-107">DESCRIPTION</span></span>
<span data-ttu-id="058b7-108">**Get-AzAlertObjectHistory** cmdlet은 경고 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="058b7-109">예제</span><span class="sxs-lookup"><span data-stu-id="058b7-109">EXAMPLES</span></span>

### <span data-ttu-id="058b7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="058b7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="058b7-111">경고 기록 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-111">Gets alert history details.</span></span> 

## <span data-ttu-id="058b7-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="058b7-112">PARAMETERS</span></span>

### <span data-ttu-id="058b7-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="058b7-113">-AlertId</span></span>
<span data-ttu-id="058b7-114">경고/ResourceId 경고의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="058b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058b7-115">-DefaultProfile</span></span>
<span data-ttu-id="058b7-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058b7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="058b7-117">-InputObject</span></span>
<span data-ttu-id="058b7-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="058b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058b7-119">CommonParameters</span></span>
<span data-ttu-id="058b7-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="058b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058b7-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="058b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058b7-122">입력</span><span class="sxs-lookup"><span data-stu-id="058b7-122">INPUTS</span></span>

### <span data-ttu-id="058b7-123">없음</span><span class="sxs-lookup"><span data-stu-id="058b7-123">None</span></span>

## <span data-ttu-id="058b7-124">출력</span><span class="sxs-lookup"><span data-stu-id="058b7-124">OUTPUTS</span></span>

### <span data-ttu-id="058b7-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="058b7-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="058b7-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="058b7-126">NOTES</span></span>

## <span data-ttu-id="058b7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="058b7-127">RELATED LINKS</span></span>
