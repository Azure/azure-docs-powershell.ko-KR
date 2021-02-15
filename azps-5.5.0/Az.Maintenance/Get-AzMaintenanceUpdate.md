---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207221"
---
# <span data-ttu-id="d30b1-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="d30b1-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="d30b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d30b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d30b1-103">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="d30b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d30b1-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d30b1-105">설명</span><span class="sxs-lookup"><span data-stu-id="d30b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d30b1-106">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="d30b1-107">예제</span><span class="sxs-lookup"><span data-stu-id="d30b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d30b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d30b1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="d30b1-109">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="d30b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d30b1-110">PARAMETERS</span></span>

### <span data-ttu-id="d30b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30b1-111">-DefaultProfile</span></span>
<span data-ttu-id="d30b1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d30b1-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="d30b1-113">-ProviderName</span></span>
<span data-ttu-id="d30b1-114">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="d30b1-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d30b1-117">-ResourceName</span></span>
<span data-ttu-id="d30b1-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="d30b1-119">-ResourceParentName</span></span>
<span data-ttu-id="d30b1-120">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="d30b1-121">-ResourceParentType</span></span>
<span data-ttu-id="d30b1-122">부모 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d30b1-123">-ResourceType</span></span>
<span data-ttu-id="d30b1-124">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30b1-125">CommonParameters</span></span>
<span data-ttu-id="d30b1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d30b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30b1-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d30b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30b1-128">입력</span><span class="sxs-lookup"><span data-stu-id="d30b1-128">INPUTS</span></span>

### <span data-ttu-id="d30b1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d30b1-129">System.String</span></span>

## <span data-ttu-id="d30b1-130">출력</span><span class="sxs-lookup"><span data-stu-id="d30b1-130">OUTPUTS</span></span>

### <span data-ttu-id="d30b1-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="d30b1-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="d30b1-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d30b1-132">NOTES</span></span>

## <span data-ttu-id="d30b1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d30b1-133">RELATED LINKS</span></span>
