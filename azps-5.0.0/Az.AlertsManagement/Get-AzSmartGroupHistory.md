---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216288"
---
# <span data-ttu-id="cf518-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="cf518-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="cf518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf518-102">SYNOPSIS</span></span>
<span data-ttu-id="cf518-103">스마트 그룹 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-103">Gets smart group history</span></span>

## <span data-ttu-id="cf518-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf518-104">SYNTAX</span></span>

### <span data-ttu-id="cf518-105">BySmartGroupId (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf518-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf518-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf518-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf518-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf518-107">DESCRIPTION</span></span>
<span data-ttu-id="cf518-108">**AzSmartGroupHistory cmdlet은** 스마트 그룹 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="cf518-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cf518-109">EXAMPLES</span></span>

### <span data-ttu-id="cf518-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf518-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="cf518-111">스마트 그룹 기록 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-111">Gets smart group history details.</span></span>

## <span data-ttu-id="cf518-112">변수</span><span class="sxs-lookup"><span data-stu-id="cf518-112">PARAMETERS</span></span>

### <span data-ttu-id="cf518-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf518-113">-DefaultProfile</span></span>
<span data-ttu-id="cf518-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf518-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf518-115">-InputObject</span></span>
<span data-ttu-id="cf518-116">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="cf518-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="cf518-117">-SmartGroupId</span></span>
<span data-ttu-id="cf518-118">경고의 SmartGroup/ResourceId의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="cf518-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf518-119">CommonParameters</span></span>
<span data-ttu-id="cf518-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf518-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf518-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf518-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf518-122">입력</span><span class="sxs-lookup"><span data-stu-id="cf518-122">INPUTS</span></span>

### <span data-ttu-id="cf518-123">않아야</span><span class="sxs-lookup"><span data-stu-id="cf518-123">None</span></span>

## <span data-ttu-id="cf518-124">출력</span><span class="sxs-lookup"><span data-stu-id="cf518-124">OUTPUTS</span></span>

### <span data-ttu-id="cf518-125">AlertsManagement 모델을 변경 합니다. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="cf518-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="cf518-126">상속자</span><span class="sxs-lookup"><span data-stu-id="cf518-126">NOTES</span></span>

## <span data-ttu-id="cf518-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf518-127">RELATED LINKS</span></span>
