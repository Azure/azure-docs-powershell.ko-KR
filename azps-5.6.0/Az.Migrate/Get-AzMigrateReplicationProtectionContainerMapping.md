---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 87fa8d8653d0409eb4b322e0ce21dbc9c8cfa668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982843"
---
# <span data-ttu-id="9c43f-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9c43f-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="9c43f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c43f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c43f-103">보호 컨테이너 매핑의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="9c43f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c43f-104">SYNTAX</span></span>

### <span data-ttu-id="9c43f-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="9c43f-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c43f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9c43f-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c43f-107">목록</span><span class="sxs-lookup"><span data-stu-id="9c43f-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c43f-108">설명</span><span class="sxs-lookup"><span data-stu-id="9c43f-108">DESCRIPTION</span></span>
<span data-ttu-id="9c43f-109">보호 컨테이너 매핑의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="9c43f-110">예제</span><span class="sxs-lookup"><span data-stu-id="9c43f-110">EXAMPLES</span></span>

### <span data-ttu-id="9c43f-111">예제 1: 특정 매핑을 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c43f-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="9c43f-112">매핑 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-112">Get a mapping detail.</span></span>

## <span data-ttu-id="9c43f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c43f-113">PARAMETERS</span></span>

### <span data-ttu-id="9c43f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c43f-114">-DefaultProfile</span></span>
<span data-ttu-id="9c43f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43f-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="9c43f-116">-FabricName</span></span>
<span data-ttu-id="9c43f-117">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43f-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="9c43f-118">-MappingName</span></span>
<span data-ttu-id="9c43f-119">보호 컨테이너 매핑 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-119">Protection Container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43f-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="9c43f-120">-ProtectionContainerName</span></span>
<span data-ttu-id="9c43f-121">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c43f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c43f-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9c43f-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9c43f-124">-ResourceName</span></span>
<span data-ttu-id="9c43f-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="9c43f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c43f-126">-SubscriptionId</span></span>
<span data-ttu-id="9c43f-127">프로젝트를 마이그레이션하는 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-127">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c43f-128">CommonParameters</span></span>
<span data-ttu-id="9c43f-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c43f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c43f-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c43f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c43f-131">입력</span><span class="sxs-lookup"><span data-stu-id="9c43f-131">INPUTS</span></span>

## <span data-ttu-id="9c43f-132">출력</span><span class="sxs-lookup"><span data-stu-id="9c43f-132">OUTPUTS</span></span>

### <span data-ttu-id="9c43f-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9c43f-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="9c43f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c43f-134">NOTES</span></span>

<span data-ttu-id="9c43f-135">별칭</span><span class="sxs-lookup"><span data-stu-id="9c43f-135">ALIASES</span></span>

## <span data-ttu-id="9c43f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c43f-136">RELATED LINKS</span></span>

