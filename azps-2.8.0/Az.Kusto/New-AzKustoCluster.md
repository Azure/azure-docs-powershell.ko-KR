---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689573"
---
# <span data-ttu-id="4381e-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4381e-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="4381e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4381e-102">SYNOPSIS</span></span>
<span data-ttu-id="4381e-103">새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="4381e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4381e-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4381e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4381e-105">DESCRIPTION</span></span>
<span data-ttu-id="4381e-106">새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="4381e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4381e-107">EXAMPLES</span></span>

### <span data-ttu-id="4381e-108">예제 1-새로운 Kusto 만들기</span><span class="sxs-lookup"><span data-stu-id="4381e-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="4381e-109">위의 명령은 리소스 그룹 "testrg"에 "mykustocluster" 이라는 새 클러스터에 대 한 새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="4381e-110">변수</span><span class="sxs-lookup"><span data-stu-id="4381e-110">PARAMETERS</span></span>

### <span data-ttu-id="4381e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4381e-111">-DefaultProfile</span></span>
<span data-ttu-id="4381e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4381e-113">-위치</span><span class="sxs-lookup"><span data-stu-id="4381e-113">-Location</span></span>
<span data-ttu-id="4381e-114">클러스터를 만들어야 하는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="4381e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4381e-115">-Name</span></span>
<span data-ttu-id="4381e-116">만들 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4381e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4381e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4381e-118">클러스터를 만들려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4381e-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="4381e-119">-Sku</span></span>
<span data-ttu-id="4381e-120">클러스터를 만드는 데 사용 되는 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="4381e-121">태그</span><span class="sxs-lookup"><span data-stu-id="4381e-121">-Tag</span></span>
<span data-ttu-id="4381e-122">이 클러스터와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4381e-123">-티어</span><span class="sxs-lookup"><span data-stu-id="4381e-123">-Tier</span></span>
<span data-ttu-id="4381e-124">클러스터를 만드는 데 사용 되는 계층 이름</span><span class="sxs-lookup"><span data-stu-id="4381e-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4381e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="4381e-125">-Confirm</span></span>
<span data-ttu-id="4381e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4381e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4381e-127">-WhatIf</span></span>
<span data-ttu-id="4381e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4381e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4381e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4381e-130">CommonParameters</span></span>
<span data-ttu-id="4381e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4381e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4381e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4381e-133">입력</span><span class="sxs-lookup"><span data-stu-id="4381e-133">INPUTS</span></span>

### <span data-ttu-id="4381e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="4381e-134">None</span></span>

## <span data-ttu-id="4381e-135">출력</span><span class="sxs-lookup"><span data-stu-id="4381e-135">OUTPUTS</span></span>

### <span data-ttu-id="4381e-136">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="4381e-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4381e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4381e-137">NOTES</span></span>

## <span data-ttu-id="4381e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4381e-138">RELATED LINKS</span></span>
