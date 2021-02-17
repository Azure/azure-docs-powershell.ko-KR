---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191212"
---
# <span data-ttu-id="cc4e6-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="cc4e6-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="cc4e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4e6-103">인시던트 소유자 개체를 만들어 인시던트 소유자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="cc4e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc4e6-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc4e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="cc4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="cc4e6-106">**New-AzSentinelIncidentOwner** cmdlet은 인시던트 업데이트를 위해 메모리에 인시던트 소유자 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="cc4e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="cc4e6-107">EXAMPLES</span></span>

### <span data-ttu-id="cc4e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc4e6-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="cc4e6-109">이 예제에서는 **IncidentOwner를 만들고** 인시던트가 새 소유자에게 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="cc4e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc4e6-110">PARAMETERS</span></span>

### <span data-ttu-id="cc4e6-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="cc4e6-111">-AssignedTo</span></span>
<span data-ttu-id="cc4e6-112">인시던트 소유자 - 할당된 인시던트 소유자</span><span class="sxs-lookup"><span data-stu-id="cc4e6-112">Incident Owner - Assigned To</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4e6-113">-DefaultProfile</span></span>
<span data-ttu-id="cc4e6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc4e6-115">-Email</span><span class="sxs-lookup"><span data-stu-id="cc4e6-115">-Email</span></span>
<span data-ttu-id="cc4e6-116">인시던트 소유자 - 전자 메일</span><span class="sxs-lookup"><span data-stu-id="cc4e6-116">Incident Owner - Email</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4e6-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc4e6-117">-ObjectId</span></span>
<span data-ttu-id="cc4e6-118">인시던트 소유자 - ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc4e6-118">Incident Owner - ObjectId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4e6-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc4e6-119">-UserPrincipalName</span></span>
<span data-ttu-id="cc4e6-120">인시던트 소유자 - 사용자 계정 이름</span><span class="sxs-lookup"><span data-stu-id="cc4e6-120">Incident Owner - User Principal Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4e6-121">CommonParameters</span></span>
<span data-ttu-id="cc4e6-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4e6-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc4e6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4e6-124">입력</span><span class="sxs-lookup"><span data-stu-id="cc4e6-124">INPUTS</span></span>

### <span data-ttu-id="cc4e6-125">없음</span><span class="sxs-lookup"><span data-stu-id="cc4e6-125">None</span></span>
## <span data-ttu-id="cc4e6-126">출력</span><span class="sxs-lookup"><span data-stu-id="cc4e6-126">OUTPUTS</span></span>

### <span data-ttu-id="cc4e6-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="cc4e6-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="cc4e6-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc4e6-128">NOTES</span></span>

## <span data-ttu-id="cc4e6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc4e6-129">RELATED LINKS</span></span>
