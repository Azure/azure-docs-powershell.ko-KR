---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219018"
---
# <span data-ttu-id="70b27-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="70b27-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="70b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70b27-102">SYNOPSIS</span></span>
<span data-ttu-id="70b27-103">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="70b27-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70b27-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70b27-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70b27-105">DESCRIPTION</span></span>
<span data-ttu-id="70b27-106">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="70b27-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70b27-107">EXAMPLES</span></span>

### <span data-ttu-id="70b27-108">예제 1: 클러스터에 대해 설정 된 모든 언어 확장 나열</span><span class="sxs-lookup"><span data-stu-id="70b27-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="70b27-109">위의 명령은 KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="70b27-110">변수</span><span class="sxs-lookup"><span data-stu-id="70b27-110">PARAMETERS</span></span>

### <span data-ttu-id="70b27-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="70b27-111">-ClusterName</span></span>
<span data-ttu-id="70b27-112">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="70b27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b27-113">-DefaultProfile</span></span>
<span data-ttu-id="70b27-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b27-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b27-115">-ResourceGroupName</span></span>
<span data-ttu-id="70b27-116">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="70b27-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70b27-117">-SubscriptionId</span></span>
<span data-ttu-id="70b27-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70b27-119">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70b27-120">-확인</span><span class="sxs-lookup"><span data-stu-id="70b27-120">-Confirm</span></span>
<span data-ttu-id="70b27-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b27-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b27-122">-WhatIf</span></span>
<span data-ttu-id="70b27-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b27-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b27-125">CommonParameters</span></span>
<span data-ttu-id="70b27-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b27-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70b27-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b27-128">입력</span><span class="sxs-lookup"><span data-stu-id="70b27-128">INPUTS</span></span>

## <span data-ttu-id="70b27-129">출력</span><span class="sxs-lookup"><span data-stu-id="70b27-129">OUTPUTS</span></span>

### <span data-ttu-id="70b27-130">Microsoft. Api20200614. ILanguageExtension에 대 한.</span><span class="sxs-lookup"><span data-stu-id="70b27-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="70b27-131">상속자</span><span class="sxs-lookup"><span data-stu-id="70b27-131">NOTES</span></span>

<span data-ttu-id="70b27-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="70b27-132">ALIASES</span></span>

## <span data-ttu-id="70b27-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70b27-133">RELATED LINKS</span></span>

