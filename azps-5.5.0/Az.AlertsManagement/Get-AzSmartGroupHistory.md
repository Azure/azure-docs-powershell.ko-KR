---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192604"
---
# <span data-ttu-id="82c8d-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="82c8d-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="82c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="82c8d-103">스마트 그룹 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-103">Gets smart group history</span></span>

## <span data-ttu-id="82c8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="82c8d-104">SYNTAX</span></span>

### <span data-ttu-id="82c8d-105">BySmartGroupId(기본값)</span><span class="sxs-lookup"><span data-stu-id="82c8d-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c8d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="82c8d-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82c8d-107">설명</span><span class="sxs-lookup"><span data-stu-id="82c8d-107">DESCRIPTION</span></span>
<span data-ttu-id="82c8d-108">**Get-AzSmartGroupHistory** cmdlet은 스마트 그룹 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="82c8d-109">예제</span><span class="sxs-lookup"><span data-stu-id="82c8d-109">EXAMPLES</span></span>

### <span data-ttu-id="82c8d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="82c8d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="82c8d-111">스마트 그룹 기록 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-111">Gets smart group history details.</span></span>

## <span data-ttu-id="82c8d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c8d-112">PARAMETERS</span></span>

### <span data-ttu-id="82c8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c8d-113">-DefaultProfile</span></span>
<span data-ttu-id="82c8d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c8d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82c8d-115">-InputObject</span></span>
<span data-ttu-id="82c8d-116">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="82c8d-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="82c8d-117">-SmartGroupId</span></span>
<span data-ttu-id="82c8d-118">경고의 SmartGroup/ResourceId의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c8d-119">CommonParameters</span></span>
<span data-ttu-id="82c8d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82c8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c8d-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82c8d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c8d-122">입력</span><span class="sxs-lookup"><span data-stu-id="82c8d-122">INPUTS</span></span>

### <span data-ttu-id="82c8d-123">없음</span><span class="sxs-lookup"><span data-stu-id="82c8d-123">None</span></span>

## <span data-ttu-id="82c8d-124">출력</span><span class="sxs-lookup"><span data-stu-id="82c8d-124">OUTPUTS</span></span>

### <span data-ttu-id="82c8d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="82c8d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="82c8d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82c8d-126">NOTES</span></span>

## <span data-ttu-id="82c8d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82c8d-127">RELATED LINKS</span></span>
