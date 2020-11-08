---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226785"
---
# <span data-ttu-id="eda2d-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eda2d-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="eda2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda2d-102">SYNOPSIS</span></span>
<span data-ttu-id="eda2d-103">보호 컨테이너의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="eda2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eda2d-104">SYNTAX</span></span>

### <span data-ttu-id="eda2d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="eda2d-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eda2d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="eda2d-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="eda2d-107">List1</span><span class="sxs-lookup"><span data-stu-id="eda2d-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eda2d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eda2d-108">DESCRIPTION</span></span>
<span data-ttu-id="eda2d-109">보호 컨테이너의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="eda2d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eda2d-110">EXAMPLES</span></span>

### <span data-ttu-id="eda2d-111">예제 1: 자격 증명 모음과 패브릭의 모든 보호 컨테이너 나열</span><span class="sxs-lookup"><span data-stu-id="eda2d-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="eda2d-112">모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-112">Lists all.</span></span>

### <span data-ttu-id="eda2d-113">예제 2: 특정 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="eda2d-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="eda2d-114">특정 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-114">Gets a specific one.</span></span>

## <span data-ttu-id="eda2d-115">변수</span><span class="sxs-lookup"><span data-stu-id="eda2d-115">PARAMETERS</span></span>

### <span data-ttu-id="eda2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda2d-116">-DefaultProfile</span></span>
<span data-ttu-id="eda2d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda2d-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="eda2d-118">-FabricName</span></span>
<span data-ttu-id="eda2d-119">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-119">Fabric name.</span></span>

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

### <span data-ttu-id="eda2d-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="eda2d-120">-ProtectionContainerName</span></span>
<span data-ttu-id="eda2d-121">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-121">Protection container name.</span></span>

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

### <span data-ttu-id="eda2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="eda2d-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="eda2d-124">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="eda2d-124">-ResourceName</span></span>
<span data-ttu-id="eda2d-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="eda2d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eda2d-126">-SubscriptionId</span></span>
<span data-ttu-id="eda2d-127">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-127">The subscription Id.</span></span>

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

### <span data-ttu-id="eda2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda2d-128">CommonParameters</span></span>
<span data-ttu-id="eda2d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda2d-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eda2d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda2d-131">입력</span><span class="sxs-lookup"><span data-stu-id="eda2d-131">INPUTS</span></span>

## <span data-ttu-id="eda2d-132">출력</span><span class="sxs-lookup"><span data-stu-id="eda2d-132">OUTPUTS</span></span>

### <span data-ttu-id="eda2d-133">Api20180110. IProtectionContainer의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="eda2d-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="eda2d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="eda2d-134">NOTES</span></span>

<span data-ttu-id="eda2d-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="eda2d-135">ALIASES</span></span>

## <span data-ttu-id="eda2d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eda2d-136">RELATED LINKS</span></span>

