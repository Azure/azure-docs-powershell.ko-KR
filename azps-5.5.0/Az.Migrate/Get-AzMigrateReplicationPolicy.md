---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: e2cad9282e1e662cee58625a17c3f0672947d26a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190172"
---
# <span data-ttu-id="1d3dc-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="1d3dc-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="1d3dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3dc-103">복제 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="1d3dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d3dc-104">SYNTAX</span></span>

### <span data-ttu-id="1d3dc-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d3dc-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1d3dc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1d3dc-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1d3dc-107">설명</span><span class="sxs-lookup"><span data-stu-id="1d3dc-107">DESCRIPTION</span></span>
<span data-ttu-id="1d3dc-108">복제 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="1d3dc-109">예제</span><span class="sxs-lookup"><span data-stu-id="1d3dc-109">EXAMPLES</span></span>

### <span data-ttu-id="1d3dc-110">예제 1: 자격 증명 모음의 모든 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="1d3dc-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="1d3dc-111">모든 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-111">Get all policies.</span></span>

### <span data-ttu-id="1d3dc-112">예제 2: 특정 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="1d3dc-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="1d3dc-113">특정 특정 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-113">Get a specific one.</span></span>

## <span data-ttu-id="1d3dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d3dc-114">PARAMETERS</span></span>

### <span data-ttu-id="1d3dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3dc-115">-DefaultProfile</span></span>
<span data-ttu-id="1d3dc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d3dc-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="1d3dc-117">-PolicyName</span></span>
<span data-ttu-id="1d3dc-118">복제 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-118">Replication policy name.</span></span>

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

### <span data-ttu-id="1d3dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d3dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d3dc-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1d3dc-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1d3dc-121">-ResourceName</span></span>
<span data-ttu-id="1d3dc-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="1d3dc-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d3dc-123">-SubscriptionId</span></span>
<span data-ttu-id="1d3dc-124">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1d3dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3dc-125">CommonParameters</span></span>
<span data-ttu-id="1d3dc-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3dc-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d3dc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3dc-128">입력</span><span class="sxs-lookup"><span data-stu-id="1d3dc-128">INPUTS</span></span>

## <span data-ttu-id="1d3dc-129">출력</span><span class="sxs-lookup"><span data-stu-id="1d3dc-129">OUTPUTS</span></span>

### <span data-ttu-id="1d3dc-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="1d3dc-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="1d3dc-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d3dc-131">NOTES</span></span>

<span data-ttu-id="1d3dc-132">별칭</span><span class="sxs-lookup"><span data-stu-id="1d3dc-132">ALIASES</span></span>

## <span data-ttu-id="1d3dc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d3dc-133">RELATED LINKS</span></span>

