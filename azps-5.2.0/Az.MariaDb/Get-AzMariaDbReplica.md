---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324148"
---
# <span data-ttu-id="e5085-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="e5085-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="e5085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5085-102">SYNOPSIS</span></span>
<span data-ttu-id="e5085-103">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="e5085-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5085-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e5085-105">설명</span><span class="sxs-lookup"><span data-stu-id="e5085-105">DESCRIPTION</span></span>
<span data-ttu-id="e5085-106">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="e5085-107">예제</span><span class="sxs-lookup"><span data-stu-id="e5085-107">EXAMPLES</span></span>

### <span data-ttu-id="e5085-108">예제 1: MariaDB 아래에 모든 복제본 DB 나열</span><span class="sxs-lookup"><span data-stu-id="e5085-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e5085-109">이 명령은 MariaDB의 모든 복제본 DB를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="e5085-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5085-110">PARAMETERS</span></span>

### <span data-ttu-id="e5085-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5085-111">-DefaultProfile</span></span>
<span data-ttu-id="e5085-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5085-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5085-113">-ResourceGroupName</span></span>
<span data-ttu-id="e5085-114">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e5085-115">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e5085-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5085-116">-ServerName</span></span>
<span data-ttu-id="e5085-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-117">The name of the server.</span></span>

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

### <span data-ttu-id="e5085-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5085-118">-SubscriptionId</span></span>
<span data-ttu-id="e5085-119">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e5085-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5085-120">CommonParameters</span></span>
<span data-ttu-id="e5085-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5085-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5085-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5085-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5085-123">입력</span><span class="sxs-lookup"><span data-stu-id="e5085-123">INPUTS</span></span>

## <span data-ttu-id="e5085-124">출력</span><span class="sxs-lookup"><span data-stu-id="e5085-124">OUTPUTS</span></span>

### <span data-ttu-id="e5085-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="e5085-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="e5085-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5085-126">NOTES</span></span>

<span data-ttu-id="e5085-127">별칭</span><span class="sxs-lookup"><span data-stu-id="e5085-127">ALIASES</span></span>

## <span data-ttu-id="e5085-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5085-128">RELATED LINKS</span></span>

