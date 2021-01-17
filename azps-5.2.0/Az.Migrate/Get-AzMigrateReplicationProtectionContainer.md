---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328117"
---
# <span data-ttu-id="21f92-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="21f92-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="21f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f92-102">SYNOPSIS</span></span>
<span data-ttu-id="21f92-103">보호 컨테이너의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="21f92-104">구문</span><span class="sxs-lookup"><span data-stu-id="21f92-104">SYNTAX</span></span>

### <span data-ttu-id="21f92-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="21f92-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21f92-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="21f92-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="21f92-107">List1</span><span class="sxs-lookup"><span data-stu-id="21f92-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="21f92-108">설명</span><span class="sxs-lookup"><span data-stu-id="21f92-108">DESCRIPTION</span></span>
<span data-ttu-id="21f92-109">보호 컨테이너의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="21f92-110">예제</span><span class="sxs-lookup"><span data-stu-id="21f92-110">EXAMPLES</span></span>

### <span data-ttu-id="21f92-111">예제 1: 자격 증명 모음 및 패브릭의 모든 보호 컨테이너 나열</span><span class="sxs-lookup"><span data-stu-id="21f92-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="21f92-112">모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-112">Lists all.</span></span>

### <span data-ttu-id="21f92-113">예제 2: 특정 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="21f92-114">특정 특정 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-114">Gets a specific one.</span></span>

## <span data-ttu-id="21f92-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21f92-115">PARAMETERS</span></span>

### <span data-ttu-id="21f92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f92-116">-DefaultProfile</span></span>
<span data-ttu-id="21f92-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f92-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="21f92-118">-FabricName</span></span>
<span data-ttu-id="21f92-119">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f92-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="21f92-120">-ProtectionContainerName</span></span>
<span data-ttu-id="21f92-121">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-121">Protection container name.</span></span>

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

### <span data-ttu-id="21f92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f92-122">-ResourceGroupName</span></span>
<span data-ttu-id="21f92-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="21f92-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="21f92-124">-ResourceName</span></span>
<span data-ttu-id="21f92-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="21f92-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21f92-126">-SubscriptionId</span></span>
<span data-ttu-id="21f92-127">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-127">The subscription Id.</span></span>

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

### <span data-ttu-id="21f92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f92-128">CommonParameters</span></span>
<span data-ttu-id="21f92-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21f92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f92-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21f92-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f92-131">입력</span><span class="sxs-lookup"><span data-stu-id="21f92-131">INPUTS</span></span>

## <span data-ttu-id="21f92-132">출력</span><span class="sxs-lookup"><span data-stu-id="21f92-132">OUTPUTS</span></span>

### <span data-ttu-id="21f92-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="21f92-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="21f92-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21f92-134">NOTES</span></span>

<span data-ttu-id="21f92-135">별칭</span><span class="sxs-lookup"><span data-stu-id="21f92-135">ALIASES</span></span>

## <span data-ttu-id="21f92-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21f92-136">RELATED LINKS</span></span>

