---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 8c0df920b8619760cf4a80d9ef6502e82de9a31f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698188"
---
# <span data-ttu-id="fbda9-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="fbda9-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="fbda9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbda9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbda9-103">알림 기록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-103">Gets Alert History information</span></span>

## <span data-ttu-id="fbda9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbda9-104">SYNTAX</span></span>

### <span data-ttu-id="fbda9-105">ByAlertId (기본값)</span><span class="sxs-lookup"><span data-stu-id="fbda9-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbda9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbda9-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbda9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fbda9-107">DESCRIPTION</span></span>
<span data-ttu-id="fbda9-108">**AzAlertObjectHistory** cmdlet은 알림 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="fbda9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fbda9-109">EXAMPLES</span></span>

### <span data-ttu-id="fbda9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbda9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="fbda9-111">알림 기록 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-111">Gets alert history details.</span></span> 

## <span data-ttu-id="fbda9-112">변수</span><span class="sxs-lookup"><span data-stu-id="fbda9-112">PARAMETERS</span></span>

### <span data-ttu-id="fbda9-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="fbda9-113">-AlertId</span></span>
<span data-ttu-id="fbda9-114">알림의 알림/ResourceId에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="fbda9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbda9-115">-DefaultProfile</span></span>
<span data-ttu-id="fbda9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbda9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbda9-117">-InputObject</span></span>
<span data-ttu-id="fbda9-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="fbda9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbda9-119">CommonParameters</span></span>
<span data-ttu-id="fbda9-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbda9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbda9-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbda9-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbda9-122">입력</span><span class="sxs-lookup"><span data-stu-id="fbda9-122">INPUTS</span></span>

### <span data-ttu-id="fbda9-123">않아야</span><span class="sxs-lookup"><span data-stu-id="fbda9-123">None</span></span>

## <span data-ttu-id="fbda9-124">출력</span><span class="sxs-lookup"><span data-stu-id="fbda9-124">OUTPUTS</span></span>

### <span data-ttu-id="fbda9-125">AlertsManagement 모델을 변경 합니다. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="fbda9-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="fbda9-126">상속자</span><span class="sxs-lookup"><span data-stu-id="fbda9-126">NOTES</span></span>

## <span data-ttu-id="fbda9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbda9-127">RELATED LINKS</span></span>