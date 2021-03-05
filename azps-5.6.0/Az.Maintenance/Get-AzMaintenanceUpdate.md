---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: dd2fb366e4e15a2c2b21c53c5bddb32bc99939ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960528"
---
# <span data-ttu-id="aa51b-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="aa51b-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="aa51b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa51b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa51b-103">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="aa51b-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa51b-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa51b-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa51b-105">DESCRIPTION</span></span>
<span data-ttu-id="aa51b-106">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="aa51b-107">예제</span><span class="sxs-lookup"><span data-stu-id="aa51b-107">EXAMPLES</span></span>

### <span data-ttu-id="aa51b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa51b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="aa51b-109">리소스에 대한 보류 중인 유지 관리 업데이트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="aa51b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa51b-110">PARAMETERS</span></span>

### <span data-ttu-id="aa51b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa51b-111">-DefaultProfile</span></span>
<span data-ttu-id="aa51b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa51b-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="aa51b-113">-ProviderName</span></span>
<span data-ttu-id="aa51b-114">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="aa51b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa51b-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa51b-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="aa51b-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aa51b-117">-ResourceName</span></span>
<span data-ttu-id="aa51b-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-118">The resource name.</span></span>

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

### <span data-ttu-id="aa51b-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="aa51b-119">-ResourceParentName</span></span>
<span data-ttu-id="aa51b-120">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-120">The parent resource name.</span></span>

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

### <span data-ttu-id="aa51b-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="aa51b-121">-ResourceParentType</span></span>
<span data-ttu-id="aa51b-122">상위 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-122">The parent resource type.</span></span>

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

### <span data-ttu-id="aa51b-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aa51b-123">-ResourceType</span></span>
<span data-ttu-id="aa51b-124">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-124">The resource type.</span></span>

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

### <span data-ttu-id="aa51b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa51b-125">CommonParameters</span></span>
<span data-ttu-id="aa51b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa51b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa51b-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa51b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa51b-128">입력</span><span class="sxs-lookup"><span data-stu-id="aa51b-128">INPUTS</span></span>

### <span data-ttu-id="aa51b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aa51b-129">System.String</span></span>

## <span data-ttu-id="aa51b-130">출력</span><span class="sxs-lookup"><span data-stu-id="aa51b-130">OUTPUTS</span></span>

### <span data-ttu-id="aa51b-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="aa51b-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="aa51b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa51b-132">NOTES</span></span>

## <span data-ttu-id="aa51b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa51b-133">RELATED LINKS</span></span>
