---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369944"
---
# <span data-ttu-id="a4740-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4740-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="a4740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4740-102">SYNOPSIS</span></span>
<span data-ttu-id="a4740-103">등록된 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="a4740-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4740-104">SYNTAX</span></span>

### <span data-ttu-id="a4740-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4740-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4740-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a4740-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4740-107">설명</span><span class="sxs-lookup"><span data-stu-id="a4740-107">DESCRIPTION</span></span>
<span data-ttu-id="a4740-108">등록된 복구 서비스 공급자의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="a4740-109">예제</span><span class="sxs-lookup"><span data-stu-id="a4740-109">EXAMPLES</span></span>

### <span data-ttu-id="a4740-110">예제 1: 자격 증명 모음의 모든 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="a4740-111">모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-111">List all.</span></span>

## <span data-ttu-id="a4740-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4740-112">PARAMETERS</span></span>

### <span data-ttu-id="a4740-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4740-113">-DefaultProfile</span></span>
<span data-ttu-id="a4740-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4740-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="a4740-115">-FabricName</span></span>
<span data-ttu-id="a4740-116">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-116">Fabric name.</span></span>

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

### <span data-ttu-id="a4740-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="a4740-117">-ProviderName</span></span>
<span data-ttu-id="a4740-118">복구 서비스 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="a4740-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="a4740-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4740-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4740-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a4740-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4740-121">-ResourceName</span></span>
<span data-ttu-id="a4740-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a4740-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4740-123">-SubscriptionId</span></span>
<span data-ttu-id="a4740-124">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-124">The subscription Id.</span></span>

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

### <span data-ttu-id="a4740-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4740-125">CommonParameters</span></span>
<span data-ttu-id="a4740-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4740-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4740-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4740-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4740-128">입력</span><span class="sxs-lookup"><span data-stu-id="a4740-128">INPUTS</span></span>

## <span data-ttu-id="a4740-129">출력</span><span class="sxs-lookup"><span data-stu-id="a4740-129">OUTPUTS</span></span>

### <span data-ttu-id="a4740-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4740-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="a4740-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4740-131">NOTES</span></span>

<span data-ttu-id="a4740-132">별칭</span><span class="sxs-lookup"><span data-stu-id="a4740-132">ALIASES</span></span>

## <span data-ttu-id="a4740-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4740-133">RELATED LINKS</span></span>

