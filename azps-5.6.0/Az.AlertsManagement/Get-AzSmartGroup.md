---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: 52060a4d7624981ee29749c4f0dba3cc8a38fda5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994644"
---
# <span data-ttu-id="7604f-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="7604f-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="7604f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7604f-102">SYNOPSIS</span></span>
<span data-ttu-id="7604f-103">스마트 그룹 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="7604f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7604f-104">SYNTAX</span></span>

### <span data-ttu-id="7604f-105">SmartGroupsListByFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="7604f-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7604f-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="7604f-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7604f-107">설명</span><span class="sxs-lookup"><span data-stu-id="7604f-107">DESCRIPTION</span></span>
<span data-ttu-id="7604f-108">**Get-AzSmartGroup** cmdlet은 스마트 그룹 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="7604f-109">예제</span><span class="sxs-lookup"><span data-stu-id="7604f-109">EXAMPLES</span></span>

### <span data-ttu-id="7604f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7604f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="7604f-111">지난 1시간 동안 형성된 모든 스마트 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="7604f-112">목록에서 Format-List 각 스마트 그룹의 전체 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="7604f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7604f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="7604f-114">ID(GUID) 또는 리소스 ID로 스마트 그룹 세부 정보 보기(id ARM 완료)</span><span class="sxs-lookup"><span data-stu-id="7604f-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="7604f-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7604f-115">PARAMETERS</span></span>

### <span data-ttu-id="7604f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7604f-116">-DefaultProfile</span></span>
<span data-ttu-id="7604f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7604f-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7604f-118">-SmartGroupId</span></span>
<span data-ttu-id="7604f-119">SmartGroup/ResourceId of SmartGroup의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7604f-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="7604f-120">-SortBy</span></span>
<span data-ttu-id="7604f-121">정렬하는 동안 사용할 경고 속성</span><span class="sxs-lookup"><span data-stu-id="7604f-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7604f-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="7604f-122">-SortOrder</span></span>
<span data-ttu-id="7604f-123">정렬 순서</span><span class="sxs-lookup"><span data-stu-id="7604f-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7604f-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="7604f-124">-TimeRange</span></span>
<span data-ttu-id="7604f-125">지원되는 시간 범위 값 - 1h, 1d, 7d, 30d(기본값은 1d)</span><span class="sxs-lookup"><span data-stu-id="7604f-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7604f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7604f-126">CommonParameters</span></span>
<span data-ttu-id="7604f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7604f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7604f-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7604f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7604f-129">입력</span><span class="sxs-lookup"><span data-stu-id="7604f-129">INPUTS</span></span>

### <span data-ttu-id="7604f-130">없음</span><span class="sxs-lookup"><span data-stu-id="7604f-130">None</span></span>

## <span data-ttu-id="7604f-131">출력</span><span class="sxs-lookup"><span data-stu-id="7604f-131">OUTPUTS</span></span>

### <span data-ttu-id="7604f-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="7604f-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="7604f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7604f-133">NOTES</span></span>

## <span data-ttu-id="7604f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7604f-134">RELATED LINKS</span></span>
