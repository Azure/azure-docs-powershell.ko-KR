---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226787"
---
# <span data-ttu-id="4de5b-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="4de5b-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="4de5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4de5b-103">Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="4de5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4de5b-104">SYNTAX</span></span>

### <span data-ttu-id="4de5b-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4de5b-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4de5b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4de5b-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4de5b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4de5b-107">DESCRIPTION</span></span>
<span data-ttu-id="4de5b-108">Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="4de5b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4de5b-109">EXAMPLES</span></span>

### <span data-ttu-id="4de5b-110">예제 1: 리소스 그룹별 모든 패브릭 및 자격 증명 모음 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="4de5b-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="4de5b-111">리소스 그룹 및 자격 증명 모음에 모든 패브릭 다운로드</span><span class="sxs-lookup"><span data-stu-id="4de5b-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="4de5b-112">예제 2: 리소스 그룹별 패브릭 가져오기, 자격 증명 모음 이름 및 패브릭 이름</span><span class="sxs-lookup"><span data-stu-id="4de5b-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="4de5b-113">특정 패브릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="4de5b-113">Get a specific fabric</span></span>

## <span data-ttu-id="4de5b-114">변수</span><span class="sxs-lookup"><span data-stu-id="4de5b-114">PARAMETERS</span></span>

### <span data-ttu-id="4de5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de5b-115">-DefaultProfile</span></span>
<span data-ttu-id="4de5b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de5b-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="4de5b-117">-FabricName</span></span>
<span data-ttu-id="4de5b-118">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-118">Fabric name.</span></span>

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

### <span data-ttu-id="4de5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4de5b-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="4de5b-121">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="4de5b-121">-ResourceName</span></span>
<span data-ttu-id="4de5b-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="4de5b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4de5b-123">-SubscriptionId</span></span>
<span data-ttu-id="4de5b-124">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-124">The subscription Id.</span></span>

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

### <span data-ttu-id="4de5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de5b-125">CommonParameters</span></span>
<span data-ttu-id="4de5b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de5b-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4de5b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de5b-128">입력</span><span class="sxs-lookup"><span data-stu-id="4de5b-128">INPUTS</span></span>

## <span data-ttu-id="4de5b-129">출력</span><span class="sxs-lookup"><span data-stu-id="4de5b-129">OUTPUTS</span></span>

### <span data-ttu-id="4de5b-130">Api20180110. IFabric의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="4de5b-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="4de5b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4de5b-131">NOTES</span></span>

<span data-ttu-id="4de5b-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="4de5b-132">ALIASES</span></span>

## <span data-ttu-id="4de5b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4de5b-133">RELATED LINKS</span></span>

