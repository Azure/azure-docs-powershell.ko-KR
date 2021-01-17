---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361852"
---
# <span data-ttu-id="c9e41-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="c9e41-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="c9e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e41-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e41-103">스마트 그룹 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="c9e41-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9e41-104">SYNTAX</span></span>

### <span data-ttu-id="c9e41-105">SmartGroupsListByFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9e41-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9e41-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="c9e41-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e41-107">설명</span><span class="sxs-lookup"><span data-stu-id="c9e41-107">DESCRIPTION</span></span>
<span data-ttu-id="c9e41-108">**Get-AzSmartGroup** cmdlet은 스마트 그룹 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="c9e41-109">예제</span><span class="sxs-lookup"><span data-stu-id="c9e41-109">EXAMPLES</span></span>

### <span data-ttu-id="c9e41-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9e41-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="c9e41-111">지난 1시간 동안 형성된 모든 스마트 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="c9e41-112">목록에서 Format-List 각 스마트 그룹의 전체 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="c9e41-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c9e41-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="c9e41-114">ID(GUID) 또는 리소스 ID로 스마트 그룹 세부 정보(전체 ARM ID)</span><span class="sxs-lookup"><span data-stu-id="c9e41-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="c9e41-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9e41-115">PARAMETERS</span></span>

### <span data-ttu-id="c9e41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e41-116">-DefaultProfile</span></span>
<span data-ttu-id="c9e41-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9e41-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c9e41-118">-SmartGroupId</span></span>
<span data-ttu-id="c9e41-119">SmartGroup/SmartGroup의 ResourceId의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="c9e41-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="c9e41-120">-SortBy</span></span>
<span data-ttu-id="c9e41-121">정렬하는 동안 사용할 경고 속성</span><span class="sxs-lookup"><span data-stu-id="c9e41-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="c9e41-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="c9e41-122">-SortOrder</span></span>
<span data-ttu-id="c9e41-123">정렬 순서</span><span class="sxs-lookup"><span data-stu-id="c9e41-123">Sort Order</span></span>

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

### <span data-ttu-id="c9e41-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="c9e41-124">-TimeRange</span></span>
<span data-ttu-id="c9e41-125">지원되는 시간 범위 값 - 1h, 1d, 7d, 30d(기본값: 1d)</span><span class="sxs-lookup"><span data-stu-id="c9e41-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="c9e41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e41-126">CommonParameters</span></span>
<span data-ttu-id="c9e41-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e41-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9e41-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e41-129">입력</span><span class="sxs-lookup"><span data-stu-id="c9e41-129">INPUTS</span></span>

### <span data-ttu-id="c9e41-130">없음</span><span class="sxs-lookup"><span data-stu-id="c9e41-130">None</span></span>

## <span data-ttu-id="c9e41-131">출력</span><span class="sxs-lookup"><span data-stu-id="c9e41-131">OUTPUTS</span></span>

### <span data-ttu-id="c9e41-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="c9e41-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="c9e41-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9e41-133">NOTES</span></span>

## <span data-ttu-id="c9e41-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9e41-134">RELATED LINKS</span></span>
