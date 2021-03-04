---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: c6ebe985d0242e626d0a417d4af3a60388cbc776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008795"
---
# <span data-ttu-id="41560-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="41560-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="41560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41560-102">SYNOPSIS</span></span>
<span data-ttu-id="41560-103">리소스에 대한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="41560-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="41560-104">구문</span><span class="sxs-lookup"><span data-stu-id="41560-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41560-105">설명</span><span class="sxs-lookup"><span data-stu-id="41560-105">DESCRIPTION</span></span>
<span data-ttu-id="41560-106">리소스에 대한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="41560-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="41560-107">예제</span><span class="sxs-lookup"><span data-stu-id="41560-107">EXAMPLES</span></span>

### <span data-ttu-id="41560-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="41560-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="41560-109">리소스에 대한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="41560-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="41560-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="41560-110">PARAMETERS</span></span>

### <span data-ttu-id="41560-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="41560-111">-ApplyUpdateName</span></span>
<span data-ttu-id="41560-112">업데이트 리소스 이름을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="41560-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41560-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41560-113">-DefaultProfile</span></span>
<span data-ttu-id="41560-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41560-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="41560-115">-ProviderName</span></span>
<span data-ttu-id="41560-116">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="41560-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41560-117">-ResourceGroupName</span></span>
<span data-ttu-id="41560-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="41560-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="41560-119">-ResourceName</span></span>
<span data-ttu-id="41560-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-120">The resource name.</span></span>

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

### <span data-ttu-id="41560-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="41560-121">-ResourceParentName</span></span>
<span data-ttu-id="41560-122">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-122">The parent resource name.</span></span>

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

### <span data-ttu-id="41560-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="41560-123">-ResourceParentType</span></span>
<span data-ttu-id="41560-124">상위 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-124">The parent resource type.</span></span>

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

### <span data-ttu-id="41560-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="41560-125">-ResourceType</span></span>
<span data-ttu-id="41560-126">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="41560-126">The resource type.</span></span>

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

### <span data-ttu-id="41560-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41560-127">CommonParameters</span></span>
<span data-ttu-id="41560-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41560-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41560-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41560-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41560-130">입력</span><span class="sxs-lookup"><span data-stu-id="41560-130">INPUTS</span></span>

### <span data-ttu-id="41560-131">System.String</span><span class="sxs-lookup"><span data-stu-id="41560-131">System.String</span></span>

## <span data-ttu-id="41560-132">출력</span><span class="sxs-lookup"><span data-stu-id="41560-132">OUTPUTS</span></span>

### <span data-ttu-id="41560-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="41560-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="41560-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41560-134">NOTES</span></span>

## <span data-ttu-id="41560-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41560-135">RELATED LINKS</span></span>
