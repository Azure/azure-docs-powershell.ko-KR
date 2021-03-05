---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 261d7467d67708380f86c8df061fdda02eb095c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982923"
---
# <span data-ttu-id="7d623-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7d623-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="7d623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d623-102">SYNOPSIS</span></span>
<span data-ttu-id="7d623-103">복제 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="7d623-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d623-104">SYNTAX</span></span>

### <span data-ttu-id="7d623-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d623-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d623-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="7d623-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7d623-107">설명</span><span class="sxs-lookup"><span data-stu-id="7d623-107">DESCRIPTION</span></span>
<span data-ttu-id="7d623-108">복제 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="7d623-109">예제</span><span class="sxs-lookup"><span data-stu-id="7d623-109">EXAMPLES</span></span>

### <span data-ttu-id="7d623-110">예제 1: 자격 증명 모음의 모든 정책 사용</span><span class="sxs-lookup"><span data-stu-id="7d623-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="7d623-111">모든 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-111">Get all policies.</span></span>

### <span data-ttu-id="7d623-112">예제 2: 특정 정책 사용</span><span class="sxs-lookup"><span data-stu-id="7d623-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="7d623-113">특정 하나를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-113">Get a specific one.</span></span>

## <span data-ttu-id="7d623-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d623-114">PARAMETERS</span></span>

### <span data-ttu-id="7d623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d623-115">-DefaultProfile</span></span>
<span data-ttu-id="7d623-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d623-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="7d623-117">-PolicyName</span></span>
<span data-ttu-id="7d623-118">복제 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-118">Replication policy name.</span></span>

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

### <span data-ttu-id="7d623-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d623-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d623-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="7d623-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7d623-121">-ResourceName</span></span>
<span data-ttu-id="7d623-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="7d623-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d623-123">-SubscriptionId</span></span>
<span data-ttu-id="7d623-124">프로젝트를 마이그레이션하는 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7d623-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d623-125">CommonParameters</span></span>
<span data-ttu-id="7d623-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d623-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d623-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d623-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d623-128">입력</span><span class="sxs-lookup"><span data-stu-id="7d623-128">INPUTS</span></span>

## <span data-ttu-id="7d623-129">출력</span><span class="sxs-lookup"><span data-stu-id="7d623-129">OUTPUTS</span></span>

### <span data-ttu-id="7d623-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="7d623-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="7d623-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d623-131">NOTES</span></span>

<span data-ttu-id="7d623-132">별칭</span><span class="sxs-lookup"><span data-stu-id="7d623-132">ALIASES</span></span>

## <span data-ttu-id="7d623-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d623-133">RELATED LINKS</span></span>

