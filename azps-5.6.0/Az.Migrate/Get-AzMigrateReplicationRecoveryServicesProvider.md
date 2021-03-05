---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982832"
---
# <span data-ttu-id="60d20-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="60d20-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="60d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60d20-102">SYNOPSIS</span></span>
<span data-ttu-id="60d20-103">등록된 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="60d20-104">구문</span><span class="sxs-lookup"><span data-stu-id="60d20-104">SYNTAX</span></span>

### <span data-ttu-id="60d20-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="60d20-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60d20-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="60d20-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="60d20-107">설명</span><span class="sxs-lookup"><span data-stu-id="60d20-107">DESCRIPTION</span></span>
<span data-ttu-id="60d20-108">등록된 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="60d20-109">예제</span><span class="sxs-lookup"><span data-stu-id="60d20-109">EXAMPLES</span></span>

### <span data-ttu-id="60d20-110">예제 1: 자격 증명 모음의 모든 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="60d20-111">모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-111">List all.</span></span>

## <span data-ttu-id="60d20-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="60d20-112">PARAMETERS</span></span>

### <span data-ttu-id="60d20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d20-113">-DefaultProfile</span></span>
<span data-ttu-id="60d20-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d20-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="60d20-115">-FabricName</span></span>
<span data-ttu-id="60d20-116">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-116">Fabric name.</span></span>

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

### <span data-ttu-id="60d20-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="60d20-117">-ProviderName</span></span>
<span data-ttu-id="60d20-118">복구 서비스 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="60d20-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="60d20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d20-119">-ResourceGroupName</span></span>
<span data-ttu-id="60d20-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="60d20-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="60d20-121">-ResourceName</span></span>
<span data-ttu-id="60d20-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="60d20-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60d20-123">-SubscriptionId</span></span>
<span data-ttu-id="60d20-124">프로젝트를 마이그레이션하는 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="60d20-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d20-125">CommonParameters</span></span>
<span data-ttu-id="60d20-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60d20-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d20-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60d20-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d20-128">입력</span><span class="sxs-lookup"><span data-stu-id="60d20-128">INPUTS</span></span>

## <span data-ttu-id="60d20-129">출력</span><span class="sxs-lookup"><span data-stu-id="60d20-129">OUTPUTS</span></span>

### <span data-ttu-id="60d20-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="60d20-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="60d20-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60d20-131">NOTES</span></span>

<span data-ttu-id="60d20-132">별칭</span><span class="sxs-lookup"><span data-stu-id="60d20-132">ALIASES</span></span>

## <span data-ttu-id="60d20-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60d20-133">RELATED LINKS</span></span>

