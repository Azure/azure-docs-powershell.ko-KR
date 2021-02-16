---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 6872eb3da4f67969dcb6ec57a9e300677bd4611b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190185"
---
# <span data-ttu-id="35222-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="35222-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="35222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35222-102">SYNOPSIS</span></span>
<span data-ttu-id="35222-103">Azure Site Recovery 패브릭의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35222-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="35222-104">구문</span><span class="sxs-lookup"><span data-stu-id="35222-104">SYNTAX</span></span>

### <span data-ttu-id="35222-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="35222-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35222-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="35222-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="35222-107">설명</span><span class="sxs-lookup"><span data-stu-id="35222-107">DESCRIPTION</span></span>
<span data-ttu-id="35222-108">Azure Site Recovery 패브릭의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35222-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="35222-109">예제</span><span class="sxs-lookup"><span data-stu-id="35222-109">EXAMPLES</span></span>

### <span data-ttu-id="35222-110">예제 1: 리소스 그룹 및 자격 증명 모음 이름으로 모든 패브릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35222-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="35222-111">리소스 그룹 및 자격 증명 모음의 모든 패브릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="35222-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="35222-112">예제 2: 리소스 그룹, 자격 증명 모음 이름 및 패브릭 이름으로 패브릭을 얻게</span><span class="sxs-lookup"><span data-stu-id="35222-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="35222-113">특정 패브릭을 얻게</span><span class="sxs-lookup"><span data-stu-id="35222-113">Get a specific fabric</span></span>

## <span data-ttu-id="35222-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35222-114">PARAMETERS</span></span>

### <span data-ttu-id="35222-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35222-115">-DefaultProfile</span></span>
<span data-ttu-id="35222-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35222-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35222-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="35222-117">-FabricName</span></span>
<span data-ttu-id="35222-118">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35222-118">Fabric name.</span></span>

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

### <span data-ttu-id="35222-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35222-119">-ResourceGroupName</span></span>
<span data-ttu-id="35222-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35222-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="35222-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="35222-121">-ResourceName</span></span>
<span data-ttu-id="35222-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35222-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="35222-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35222-123">-SubscriptionId</span></span>
<span data-ttu-id="35222-124">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35222-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="35222-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35222-125">CommonParameters</span></span>
<span data-ttu-id="35222-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35222-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35222-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35222-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35222-128">입력</span><span class="sxs-lookup"><span data-stu-id="35222-128">INPUTS</span></span>

## <span data-ttu-id="35222-129">출력</span><span class="sxs-lookup"><span data-stu-id="35222-129">OUTPUTS</span></span>

### <span data-ttu-id="35222-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="35222-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="35222-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35222-131">NOTES</span></span>

<span data-ttu-id="35222-132">별칭</span><span class="sxs-lookup"><span data-stu-id="35222-132">ALIASES</span></span>

## <span data-ttu-id="35222-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35222-133">RELATED LINKS</span></span>

