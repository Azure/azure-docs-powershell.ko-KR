---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94055997"
---
# <span data-ttu-id="07e53-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="07e53-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="07e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e53-102">SYNOPSIS</span></span>
<span data-ttu-id="07e53-103">알림 기록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-103">Gets Alert History information</span></span>

## <span data-ttu-id="07e53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07e53-104">SYNTAX</span></span>

### <span data-ttu-id="07e53-105">ByAlertId (기본값)</span><span class="sxs-lookup"><span data-stu-id="07e53-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e53-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07e53-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07e53-107">설명은</span><span class="sxs-lookup"><span data-stu-id="07e53-107">DESCRIPTION</span></span>
<span data-ttu-id="07e53-108">**AzAlertObjectHistory** cmdlet은 알림 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="07e53-109">예제의</span><span class="sxs-lookup"><span data-stu-id="07e53-109">EXAMPLES</span></span>

### <span data-ttu-id="07e53-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="07e53-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="07e53-111">알림 기록 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-111">Gets alert history details.</span></span> 

## <span data-ttu-id="07e53-112">변수</span><span class="sxs-lookup"><span data-stu-id="07e53-112">PARAMETERS</span></span>

### <span data-ttu-id="07e53-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="07e53-113">-AlertId</span></span>
<span data-ttu-id="07e53-114">알림의 알림/ResourceId에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="07e53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e53-115">-DefaultProfile</span></span>
<span data-ttu-id="07e53-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07e53-117">-InputObject</span></span>
<span data-ttu-id="07e53-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="07e53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e53-119">CommonParameters</span></span>
<span data-ttu-id="07e53-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07e53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e53-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07e53-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e53-122">입력</span><span class="sxs-lookup"><span data-stu-id="07e53-122">INPUTS</span></span>

### <span data-ttu-id="07e53-123">않아야</span><span class="sxs-lookup"><span data-stu-id="07e53-123">None</span></span>

## <span data-ttu-id="07e53-124">출력</span><span class="sxs-lookup"><span data-stu-id="07e53-124">OUTPUTS</span></span>

### <span data-ttu-id="07e53-125">AlertsManagement 모델을 변경 합니다. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="07e53-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="07e53-126">상속자</span><span class="sxs-lookup"><span data-stu-id="07e53-126">NOTES</span></span>

## <span data-ttu-id="07e53-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07e53-127">RELATED LINKS</span></span>
