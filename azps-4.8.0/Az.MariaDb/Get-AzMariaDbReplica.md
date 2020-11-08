---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056273"
---
# <span data-ttu-id="4c230-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="4c230-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="4c230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c230-102">SYNOPSIS</span></span>
<span data-ttu-id="4c230-103">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4c230-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c230-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4c230-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4c230-105">DESCRIPTION</span></span>
<span data-ttu-id="4c230-106">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4c230-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4c230-107">EXAMPLES</span></span>

### <span data-ttu-id="4c230-108">예제 1: 모든 복제 DB를 a: \ b에 나열</span><span class="sxs-lookup"><span data-stu-id="4c230-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4c230-109">이 명령은 모든 복제 DB를 a 2 i a b 아래에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="4c230-110">변수</span><span class="sxs-lookup"><span data-stu-id="4c230-110">PARAMETERS</span></span>

### <span data-ttu-id="4c230-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c230-111">-DefaultProfile</span></span>
<span data-ttu-id="4c230-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c230-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c230-113">-ResourceGroupName</span></span>
<span data-ttu-id="4c230-114">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4c230-115">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4c230-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c230-116">-ServerName</span></span>
<span data-ttu-id="4c230-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-117">The name of the server.</span></span>

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

### <span data-ttu-id="4c230-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c230-118">-SubscriptionId</span></span>
<span data-ttu-id="4c230-119">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4c230-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c230-120">CommonParameters</span></span>
<span data-ttu-id="4c230-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c230-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c230-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4c230-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c230-123">입력</span><span class="sxs-lookup"><span data-stu-id="4c230-123">INPUTS</span></span>

## <span data-ttu-id="4c230-124">출력</span><span class="sxs-lookup"><span data-stu-id="4c230-124">OUTPUTS</span></span>

### <span data-ttu-id="4c230-125">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="4c230-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4c230-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4c230-126">NOTES</span></span>

<span data-ttu-id="4c230-127">별칭과</span><span class="sxs-lookup"><span data-stu-id="4c230-127">ALIASES</span></span>

## <span data-ttu-id="4c230-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c230-128">RELATED LINKS</span></span>

