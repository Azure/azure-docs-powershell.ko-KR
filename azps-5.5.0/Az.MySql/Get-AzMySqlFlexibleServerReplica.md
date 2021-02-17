---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192129"
---
# <span data-ttu-id="51861-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="51861-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="51861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51861-102">SYNOPSIS</span></span>
<span data-ttu-id="51861-103">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="51861-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="51861-104">구문</span><span class="sxs-lookup"><span data-stu-id="51861-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="51861-105">설명</span><span class="sxs-lookup"><span data-stu-id="51861-105">DESCRIPTION</span></span>
<span data-ttu-id="51861-106">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="51861-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="51861-107">예제</span><span class="sxs-lookup"><span data-stu-id="51861-107">EXAMPLES</span></span>

### <span data-ttu-id="51861-108">예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 복제본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51861-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="51861-109">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버 복제본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51861-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="51861-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51861-110">PARAMETERS</span></span>

### <span data-ttu-id="51861-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51861-111">-DefaultProfile</span></span>
<span data-ttu-id="51861-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51861-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51861-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51861-113">-ResourceGroupName</span></span>
<span data-ttu-id="51861-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51861-114">The name of the resource group.</span></span>
<span data-ttu-id="51861-115">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="51861-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="51861-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51861-116">-ServerName</span></span>
<span data-ttu-id="51861-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51861-117">The name of the server.</span></span>

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

### <span data-ttu-id="51861-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51861-118">-SubscriptionId</span></span>
<span data-ttu-id="51861-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51861-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="51861-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51861-120">CommonParameters</span></span>
<span data-ttu-id="51861-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51861-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51861-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51861-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51861-123">입력</span><span class="sxs-lookup"><span data-stu-id="51861-123">INPUTS</span></span>

## <span data-ttu-id="51861-124">출력</span><span class="sxs-lookup"><span data-stu-id="51861-124">OUTPUTS</span></span>

### <span data-ttu-id="51861-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="51861-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="51861-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51861-126">NOTES</span></span>

<span data-ttu-id="51861-127">별칭</span><span class="sxs-lookup"><span data-stu-id="51861-127">ALIASES</span></span>

## <span data-ttu-id="51861-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51861-128">RELATED LINKS</span></span>

