---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216287"
---
# <span data-ttu-id="0f8bf-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="0f8bf-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="0f8bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8bf-103">스마트 그룹 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="0f8bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f8bf-104">SYNTAX</span></span>

### <span data-ttu-id="0f8bf-105">Smart2| Listbyfilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f8bf-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="0f8bf-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f8bf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f8bf-107">DESCRIPTION</span></span>
<span data-ttu-id="0f8bf-108">**AzSmartGroup cmdlet은** 스마트 그룹 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="0f8bf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f8bf-109">EXAMPLES</span></span>

### <span data-ttu-id="0f8bf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f8bf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="0f8bf-111">지난 1 시간 동안 형성 된 모든 스마트 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="0f8bf-112">Format-List를 사용 하 여 목록의 각 스마트 그룹에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="0f8bf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0f8bf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="0f8bf-114">Id (GUID) 또는 리소스 Id로 스마트 그룹 세부 정보 가져오기 (전체 팔 Id)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="0f8bf-115">변수</span><span class="sxs-lookup"><span data-stu-id="0f8bf-115">PARAMETERS</span></span>

### <span data-ttu-id="0f8bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8bf-116">-DefaultProfile</span></span>
<span data-ttu-id="0f8bf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f8bf-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0f8bf-118">-SmartGroupId</span></span>
<span data-ttu-id="0f8bf-119">SmartGroup의 SmartGroup/ResourceId의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="0f8bf-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="0f8bf-120">-SortBy</span></span>
<span data-ttu-id="0f8bf-121">정렬 하는 동안 사용할 알림 속성</span><span class="sxs-lookup"><span data-stu-id="0f8bf-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="0f8bf-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="0f8bf-122">-SortOrder</span></span>
<span data-ttu-id="0f8bf-123">정렬 순서</span><span class="sxs-lookup"><span data-stu-id="0f8bf-123">Sort Order</span></span>

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

### <span data-ttu-id="0f8bf-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="0f8bf-124">-TimeRange</span></span>
<span data-ttu-id="0f8bf-125">지원 되는 시간 범위 값-1h, 1d, 7d, 30d (기본값은 1d)</span><span class="sxs-lookup"><span data-stu-id="0f8bf-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="0f8bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8bf-126">CommonParameters</span></span>
<span data-ttu-id="0f8bf-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8bf-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f8bf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8bf-129">입력</span><span class="sxs-lookup"><span data-stu-id="0f8bf-129">INPUTS</span></span>

### <span data-ttu-id="0f8bf-130">않아야</span><span class="sxs-lookup"><span data-stu-id="0f8bf-130">None</span></span>

## <span data-ttu-id="0f8bf-131">출력</span><span class="sxs-lookup"><span data-stu-id="0f8bf-131">OUTPUTS</span></span>

### <span data-ttu-id="0f8bf-132">AlertsManagement 모델. a PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="0f8bf-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="0f8bf-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0f8bf-133">NOTES</span></span>

## <span data-ttu-id="0f8bf-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f8bf-134">RELATED LINKS</span></span>
