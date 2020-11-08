---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211645"
---
# <span data-ttu-id="1a10d-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="1a10d-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="1a10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a10d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a10d-103">리소스에 대 한 보류 중인 유지 관리 업데이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="1a10d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a10d-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a10d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a10d-105">DESCRIPTION</span></span>
<span data-ttu-id="1a10d-106">리소스에 대 한 보류 중인 유지 관리 업데이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="1a10d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a10d-107">EXAMPLES</span></span>

### <span data-ttu-id="1a10d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a10d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="1a10d-109">리소스에 대 한 보류 중인 유지 관리 업데이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="1a10d-110">변수</span><span class="sxs-lookup"><span data-stu-id="1a10d-110">PARAMETERS</span></span>

### <span data-ttu-id="1a10d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a10d-111">-DefaultProfile</span></span>
<span data-ttu-id="1a10d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a10d-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="1a10d-113">-ProviderName</span></span>
<span data-ttu-id="1a10d-114">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="1a10d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a10d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a10d-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="1a10d-117">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="1a10d-117">-ResourceName</span></span>
<span data-ttu-id="1a10d-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-118">The resource name.</span></span>

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

### <span data-ttu-id="1a10d-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="1a10d-119">-ResourceParentName</span></span>
<span data-ttu-id="1a10d-120">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-120">The parent resource name.</span></span>

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

### <span data-ttu-id="1a10d-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="1a10d-121">-ResourceParentType</span></span>
<span data-ttu-id="1a10d-122">부모 리소스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-122">The parent resource type.</span></span>

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

### <span data-ttu-id="1a10d-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1a10d-123">-ResourceType</span></span>
<span data-ttu-id="1a10d-124">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-124">The resource type.</span></span>

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

### <span data-ttu-id="1a10d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a10d-125">CommonParameters</span></span>
<span data-ttu-id="1a10d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a10d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a10d-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a10d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a10d-128">입력</span><span class="sxs-lookup"><span data-stu-id="1a10d-128">INPUTS</span></span>

### <span data-ttu-id="1a10d-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a10d-129">System.String</span></span>

## <span data-ttu-id="1a10d-130">출력</span><span class="sxs-lookup"><span data-stu-id="1a10d-130">OUTPUTS</span></span>

### <span data-ttu-id="1a10d-131">Microsoft. Azure. 관리. 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a10d-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="1a10d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1a10d-132">NOTES</span></span>

## <span data-ttu-id="1a10d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a10d-133">RELATED LINKS</span></span>
