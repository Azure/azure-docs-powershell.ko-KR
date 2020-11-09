---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304538"
---
# <span data-ttu-id="b0721-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="b0721-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="b0721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0721-102">SYNOPSIS</span></span>
<span data-ttu-id="b0721-103">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b0721-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0721-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b0721-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0721-105">DESCRIPTION</span></span>
<span data-ttu-id="b0721-106">지정 된 서버의 모든 복제본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b0721-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0721-107">EXAMPLES</span></span>

### <span data-ttu-id="b0721-108">예제 1: 리소스 그룹별 MySql server 복제본 가져오기 및 서버 이름</span><span class="sxs-lookup"><span data-stu-id="b0721-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b0721-109">이 cmdlet은 리소스 그룹 및 서버 이름에 따라 MySql 서버 복제본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="b0721-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0721-110">PARAMETERS</span></span>

### <span data-ttu-id="b0721-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0721-111">-DefaultProfile</span></span>
<span data-ttu-id="b0721-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0721-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0721-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0721-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-114">The name of the resource group.</span></span>
<span data-ttu-id="b0721-115">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b0721-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0721-116">-ServerName</span></span>
<span data-ttu-id="b0721-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-117">The name of the server.</span></span>

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

### <span data-ttu-id="b0721-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0721-118">-SubscriptionId</span></span>
<span data-ttu-id="b0721-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b0721-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0721-120">CommonParameters</span></span>
<span data-ttu-id="b0721-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0721-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0721-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0721-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0721-123">입력</span><span class="sxs-lookup"><span data-stu-id="b0721-123">INPUTS</span></span>

## <span data-ttu-id="b0721-124">출력</span><span class="sxs-lookup"><span data-stu-id="b0721-124">OUTPUTS</span></span>

### <span data-ttu-id="b0721-125">Api20171201 (Microsoft. i m/. i m/. i m/. 서버)</span><span class="sxs-lookup"><span data-stu-id="b0721-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b0721-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b0721-126">NOTES</span></span>

<span data-ttu-id="b0721-127">별칭과</span><span class="sxs-lookup"><span data-stu-id="b0721-127">ALIASES</span></span>

## <span data-ttu-id="b0721-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0721-128">RELATED LINKS</span></span>

