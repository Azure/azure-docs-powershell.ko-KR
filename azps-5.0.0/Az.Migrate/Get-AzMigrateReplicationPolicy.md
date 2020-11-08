---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226786"
---
# <span data-ttu-id="54679-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="54679-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="54679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54679-102">SYNOPSIS</span></span>
<span data-ttu-id="54679-103">복제 정책의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54679-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="54679-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54679-104">SYNTAX</span></span>

### <span data-ttu-id="54679-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="54679-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54679-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="54679-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="54679-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54679-107">DESCRIPTION</span></span>
<span data-ttu-id="54679-108">복제 정책의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54679-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="54679-109">예제의</span><span class="sxs-lookup"><span data-stu-id="54679-109">EXAMPLES</span></span>

### <span data-ttu-id="54679-110">예제 1: 자격 증명 모음에서 모든 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="54679-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="54679-111">모든 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54679-111">Get all policies.</span></span>

### <span data-ttu-id="54679-112">예제 2: 특정 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="54679-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="54679-113">특정 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54679-113">Get a specific one.</span></span>

## <span data-ttu-id="54679-114">변수</span><span class="sxs-lookup"><span data-stu-id="54679-114">PARAMETERS</span></span>

### <span data-ttu-id="54679-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54679-115">-DefaultProfile</span></span>
<span data-ttu-id="54679-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54679-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54679-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="54679-117">-PolicyName</span></span>
<span data-ttu-id="54679-118">복제 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54679-118">Replication policy name.</span></span>

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

### <span data-ttu-id="54679-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54679-119">-ResourceGroupName</span></span>
<span data-ttu-id="54679-120">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54679-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="54679-121">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="54679-121">-ResourceName</span></span>
<span data-ttu-id="54679-122">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54679-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="54679-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54679-123">-SubscriptionId</span></span>
<span data-ttu-id="54679-124">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54679-124">The subscription Id.</span></span>

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

### <span data-ttu-id="54679-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54679-125">CommonParameters</span></span>
<span data-ttu-id="54679-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54679-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54679-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54679-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54679-128">입력</span><span class="sxs-lookup"><span data-stu-id="54679-128">INPUTS</span></span>

## <span data-ttu-id="54679-129">출력</span><span class="sxs-lookup"><span data-stu-id="54679-129">OUTPUTS</span></span>

### <span data-ttu-id="54679-130">Api20180110 (Microsoft. PowerShell. .exe 정책)</span><span class="sxs-lookup"><span data-stu-id="54679-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="54679-131">상속자</span><span class="sxs-lookup"><span data-stu-id="54679-131">NOTES</span></span>

<span data-ttu-id="54679-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="54679-132">ALIASES</span></span>

## <span data-ttu-id="54679-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54679-133">RELATED LINKS</span></span>

