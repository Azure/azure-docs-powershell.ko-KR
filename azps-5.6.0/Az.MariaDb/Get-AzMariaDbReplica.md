---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970656"
---
# <span data-ttu-id="e999a-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="e999a-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="e999a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e999a-102">SYNOPSIS</span></span>
<span data-ttu-id="e999a-103">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="e999a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e999a-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e999a-105">설명</span><span class="sxs-lookup"><span data-stu-id="e999a-105">DESCRIPTION</span></span>
<span data-ttu-id="e999a-106">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="e999a-107">예제</span><span class="sxs-lookup"><span data-stu-id="e999a-107">EXAMPLES</span></span>

### <span data-ttu-id="e999a-108">예제 1: MariaDB 아래에 모든 복제본 DB 나열</span><span class="sxs-lookup"><span data-stu-id="e999a-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e999a-109">이 명령은 MariaDB 아래에 있는 모든 복제본 DB를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="e999a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e999a-110">PARAMETERS</span></span>

### <span data-ttu-id="e999a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e999a-111">-DefaultProfile</span></span>
<span data-ttu-id="e999a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e999a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e999a-113">-ResourceGroupName</span></span>
<span data-ttu-id="e999a-114">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e999a-115">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e999a-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e999a-116">-ServerName</span></span>
<span data-ttu-id="e999a-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-117">The name of the server.</span></span>

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

### <span data-ttu-id="e999a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e999a-118">-SubscriptionId</span></span>
<span data-ttu-id="e999a-119">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e999a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e999a-120">CommonParameters</span></span>
<span data-ttu-id="e999a-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e999a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e999a-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e999a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e999a-123">입력</span><span class="sxs-lookup"><span data-stu-id="e999a-123">INPUTS</span></span>

## <span data-ttu-id="e999a-124">출력</span><span class="sxs-lookup"><span data-stu-id="e999a-124">OUTPUTS</span></span>

### <span data-ttu-id="e999a-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="e999a-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="e999a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e999a-126">NOTES</span></span>

<span data-ttu-id="e999a-127">별칭</span><span class="sxs-lookup"><span data-stu-id="e999a-127">ALIASES</span></span>

## <span data-ttu-id="e999a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e999a-128">RELATED LINKS</span></span>

