---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226782"
---
# <span data-ttu-id="06407-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="06407-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="06407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06407-102">SYNOPSIS</span></span>
<span data-ttu-id="06407-103">보호 컨테이너 매핑의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06407-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="06407-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06407-104">SYNTAX</span></span>

### <span data-ttu-id="06407-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="06407-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06407-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="06407-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06407-107">목록</span><span class="sxs-lookup"><span data-stu-id="06407-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="06407-108">설명은</span><span class="sxs-lookup"><span data-stu-id="06407-108">DESCRIPTION</span></span>
<span data-ttu-id="06407-109">보호 컨테이너 매핑의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06407-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="06407-110">예제의</span><span class="sxs-lookup"><span data-stu-id="06407-110">EXAMPLES</span></span>

### <span data-ttu-id="06407-111">예제 1: 특정 매핑 가져오기</span><span class="sxs-lookup"><span data-stu-id="06407-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="06407-112">매핑 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06407-112">Get a mapping detail.</span></span>

## <span data-ttu-id="06407-113">변수</span><span class="sxs-lookup"><span data-stu-id="06407-113">PARAMETERS</span></span>

### <span data-ttu-id="06407-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06407-114">-DefaultProfile</span></span>
<span data-ttu-id="06407-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06407-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="06407-116">-FabricName</span></span>
<span data-ttu-id="06407-117">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-117">Fabric name.</span></span>

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

### <span data-ttu-id="06407-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="06407-118">-MappingName</span></span>
<span data-ttu-id="06407-119">보호 컨테이너 매핑 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="06407-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="06407-120">-ProtectionContainerName</span></span>
<span data-ttu-id="06407-121">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-121">Protection container name.</span></span>

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

### <span data-ttu-id="06407-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06407-122">-ResourceGroupName</span></span>
<span data-ttu-id="06407-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="06407-124">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="06407-124">-ResourceName</span></span>
<span data-ttu-id="06407-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="06407-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06407-126">-SubscriptionId</span></span>
<span data-ttu-id="06407-127">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="06407-127">The subscription Id.</span></span>

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

### <span data-ttu-id="06407-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06407-128">CommonParameters</span></span>
<span data-ttu-id="06407-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06407-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06407-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06407-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06407-131">입력</span><span class="sxs-lookup"><span data-stu-id="06407-131">INPUTS</span></span>

## <span data-ttu-id="06407-132">출력</span><span class="sxs-lookup"><span data-stu-id="06407-132">OUTPUTS</span></span>

### <span data-ttu-id="06407-133">Api20180110. IProtectionContainerMapping의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="06407-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="06407-134">상속자</span><span class="sxs-lookup"><span data-stu-id="06407-134">NOTES</span></span>

<span data-ttu-id="06407-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="06407-135">ALIASES</span></span>

## <span data-ttu-id="06407-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06407-136">RELATED LINKS</span></span>

