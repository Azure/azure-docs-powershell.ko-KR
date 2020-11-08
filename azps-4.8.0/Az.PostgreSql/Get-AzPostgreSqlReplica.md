---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214268"
---
# <span data-ttu-id="69d02-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="69d02-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="69d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d02-102">SYNOPSIS</span></span>
<span data-ttu-id="69d02-103">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="69d02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69d02-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="69d02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69d02-105">DESCRIPTION</span></span>
<span data-ttu-id="69d02-106">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="69d02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69d02-107">EXAMPLES</span></span>

### <span data-ttu-id="69d02-108">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 복제본 가져오기</span><span class="sxs-lookup"><span data-stu-id="69d02-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="69d02-109">이 cmdlet은 리소스 그룹과 서버 이름으로 PostgreSql 서버 복제본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="69d02-110">변수</span><span class="sxs-lookup"><span data-stu-id="69d02-110">PARAMETERS</span></span>

### <span data-ttu-id="69d02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d02-111">-DefaultProfile</span></span>
<span data-ttu-id="69d02-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69d02-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69d02-113">-ResourceGroupName</span></span>
<span data-ttu-id="69d02-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-114">The name of the resource group.</span></span>
<span data-ttu-id="69d02-115">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="69d02-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69d02-116">-ServerName</span></span>
<span data-ttu-id="69d02-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-117">The name of the server.</span></span>

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

### <span data-ttu-id="69d02-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69d02-118">-SubscriptionId</span></span>
<span data-ttu-id="69d02-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="69d02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d02-120">CommonParameters</span></span>
<span data-ttu-id="69d02-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d02-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69d02-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d02-123">입력</span><span class="sxs-lookup"><span data-stu-id="69d02-123">INPUTS</span></span>

## <span data-ttu-id="69d02-124">출력</span><span class="sxs-lookup"><span data-stu-id="69d02-124">OUTPUTS</span></span>

### <span data-ttu-id="69d02-125">PostgreSql. Api20171201. i m m.</span><span class="sxs-lookup"><span data-stu-id="69d02-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="69d02-126">상속자</span><span class="sxs-lookup"><span data-stu-id="69d02-126">NOTES</span></span>

<span data-ttu-id="69d02-127">별칭과</span><span class="sxs-lookup"><span data-stu-id="69d02-127">ALIASES</span></span>

## <span data-ttu-id="69d02-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69d02-128">RELATED LINKS</span></span>

