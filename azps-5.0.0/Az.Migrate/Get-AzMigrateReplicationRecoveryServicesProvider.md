---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226779"
---
# <span data-ttu-id="ceedf-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ceedf-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="ceedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceedf-102">SYNOPSIS</span></span>
<span data-ttu-id="ceedf-103">등록 된 복구 서비스 공급자의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ceedf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ceedf-104">SYNTAX</span></span>

### <span data-ttu-id="ceedf-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ceedf-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ceedf-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ceedf-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ceedf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ceedf-107">DESCRIPTION</span></span>
<span data-ttu-id="ceedf-108">등록 된 복구 서비스 공급자의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ceedf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ceedf-109">EXAMPLES</span></span>

### <span data-ttu-id="ceedf-110">예제 1: 자격 증명 모음에 모든 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="ceedf-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="ceedf-111">모두 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-111">List all.</span></span>

## <span data-ttu-id="ceedf-112">변수</span><span class="sxs-lookup"><span data-stu-id="ceedf-112">PARAMETERS</span></span>

### <span data-ttu-id="ceedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceedf-113">-DefaultProfile</span></span>
<span data-ttu-id="ceedf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceedf-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="ceedf-115">-FabricName</span></span>
<span data-ttu-id="ceedf-116">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-116">Fabric name.</span></span>

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

### <span data-ttu-id="ceedf-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ceedf-117">-ProviderName</span></span>
<span data-ttu-id="ceedf-118">Recovery services 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="ceedf-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="ceedf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceedf-119">-ResourceGroupName</span></span>
<span data-ttu-id="ceedf-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="ceedf-121">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="ceedf-121">-ResourceName</span></span>
<span data-ttu-id="ceedf-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="ceedf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ceedf-123">-SubscriptionId</span></span>
<span data-ttu-id="ceedf-124">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-124">The subscription Id.</span></span>

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

### <span data-ttu-id="ceedf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceedf-125">CommonParameters</span></span>
<span data-ttu-id="ceedf-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceedf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceedf-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ceedf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceedf-128">입력</span><span class="sxs-lookup"><span data-stu-id="ceedf-128">INPUTS</span></span>

## <span data-ttu-id="ceedf-129">출력</span><span class="sxs-lookup"><span data-stu-id="ceedf-129">OUTPUTS</span></span>

### <span data-ttu-id="ceedf-130">Api20180110. Irecovery서비스 공급자가 제공 하는 PowerShell</span><span class="sxs-lookup"><span data-stu-id="ceedf-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="ceedf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ceedf-131">NOTES</span></span>

<span data-ttu-id="ceedf-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="ceedf-132">ALIASES</span></span>

## <span data-ttu-id="ceedf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceedf-133">RELATED LINKS</span></span>

