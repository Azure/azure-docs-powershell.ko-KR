---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867802"
---
# <span data-ttu-id="e5796-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="e5796-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="e5796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5796-102">SYNOPSIS</span></span>
<span data-ttu-id="e5796-103">기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="e5796-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5796-104">SYNTAX</span></span>

### <span data-ttu-id="e5796-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5796-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5796-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5796-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5796-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5796-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5796-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e5796-108">DESCRIPTION</span></span>
<span data-ttu-id="e5796-109">기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="e5796-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e5796-110">EXAMPLES</span></span>

### <span data-ttu-id="e5796-111">예제 1-이름으로 기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="e5796-112">위의 명령은 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터에서 "mykustodatabase" 이라는 이름으로 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="e5796-113">예제 2-파이핑을 통해 기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="e5796-114">위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터에서 "mykustodatabase" 이라는 이름의 "이름" 데이터베이스를 가져온 `Get-AzKustoDatabase` 다음 결과를 `Remove-AzKustoDatabase` 삭제 하도록 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="e5796-115">변수</span><span class="sxs-lookup"><span data-stu-id="e5796-115">PARAMETERS</span></span>

### <span data-ttu-id="e5796-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e5796-116">-ClusterName</span></span>
<span data-ttu-id="e5796-117">데이터베이스가 있는 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5796-118">-DefaultProfile</span></span>
<span data-ttu-id="e5796-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5796-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5796-120">-InputObject</span></span>
<span data-ttu-id="e5796-121">데이터베이스 개체에는 kusto가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e5796-122">-Name</span></span>
<span data-ttu-id="e5796-123">제거할 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5796-124">-PassThru</span></span>
<span data-ttu-id="e5796-125">지정 된 데이터베이스가 성공적으로 일시 중단 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-125">Return whether the specified database was successfully suspended or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5796-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5796-127">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5796-128">-ResourceId</span></span>
<span data-ttu-id="e5796-129">데이터베이스 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="e5796-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5796-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e5796-130">-Confirm</span></span>
<span data-ttu-id="e5796-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5796-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5796-132">-WhatIf</span></span>
<span data-ttu-id="e5796-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5796-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5796-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5796-135">CommonParameters</span></span>
<span data-ttu-id="e5796-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5796-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5796-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5796-138">입력</span><span class="sxs-lookup"><span data-stu-id="e5796-138">INPUTS</span></span>

### <span data-ttu-id="e5796-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5796-139">System.String</span></span>

### <span data-ttu-id="e5796-140">PSKustoDatabase를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e5796-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="e5796-141">출력</span><span class="sxs-lookup"><span data-stu-id="e5796-141">OUTPUTS</span></span>

### <span data-ttu-id="e5796-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e5796-142">System.Boolean</span></span>

## <span data-ttu-id="e5796-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e5796-143">NOTES</span></span>

## <span data-ttu-id="e5796-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5796-144">RELATED LINKS</span></span>
