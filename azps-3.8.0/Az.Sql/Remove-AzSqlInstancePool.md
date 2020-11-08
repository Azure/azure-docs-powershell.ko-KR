---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042945"
---
# <span data-ttu-id="63247-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="63247-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="63247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63247-102">SYNOPSIS</span></span>
<span data-ttu-id="63247-103">Azure SQL 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63247-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="63247-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63247-104">SYNTAX</span></span>

### <span data-ttu-id="63247-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="63247-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63247-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63247-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63247-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63247-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63247-108">설명은</span><span class="sxs-lookup"><span data-stu-id="63247-108">DESCRIPTION</span></span>
<span data-ttu-id="63247-109">**AzSqlInstancePool** Cmdlet은 Azure SQL 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63247-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="63247-110">예제의</span><span class="sxs-lookup"><span data-stu-id="63247-110">EXAMPLES</span></span>

### <span data-ttu-id="63247-111">예제 1: 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="63247-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="63247-112">예제 2: 리소스 식별자를 기준으로 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="63247-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="63247-113">예제 3: 인스턴스 풀 개체를 기준으로 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="63247-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="63247-114">이 명령은 instancePool0 이라는 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63247-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="63247-115">변수</span><span class="sxs-lookup"><span data-stu-id="63247-115">PARAMETERS</span></span>

### <span data-ttu-id="63247-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63247-116">-DefaultProfile</span></span>
<span data-ttu-id="63247-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63247-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63247-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63247-118">-InputObject</span></span>
<span data-ttu-id="63247-119">제거할 인스턴스 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="63247-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63247-120">-이름</span><span class="sxs-lookup"><span data-stu-id="63247-120">-Name</span></span>
<span data-ttu-id="63247-121">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63247-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63247-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63247-122">-ResourceGroupName</span></span>
<span data-ttu-id="63247-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63247-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63247-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63247-124">-ResourceId</span></span>
<span data-ttu-id="63247-125">제거할 인스턴스 풀 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="63247-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63247-126">-확인</span><span class="sxs-lookup"><span data-stu-id="63247-126">-Confirm</span></span>
<span data-ttu-id="63247-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63247-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63247-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63247-128">-WhatIf</span></span>
<span data-ttu-id="63247-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63247-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63247-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63247-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63247-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63247-131">CommonParameters</span></span>
<span data-ttu-id="63247-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63247-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63247-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63247-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63247-134">입력</span><span class="sxs-lookup"><span data-stu-id="63247-134">INPUTS</span></span>

### <span data-ttu-id="63247-135">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="63247-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="63247-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63247-136">System.String</span></span>

## <span data-ttu-id="63247-137">출력</span><span class="sxs-lookup"><span data-stu-id="63247-137">OUTPUTS</span></span>

### <span data-ttu-id="63247-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="63247-138">System.Object</span></span>
## <span data-ttu-id="63247-139">상속자</span><span class="sxs-lookup"><span data-stu-id="63247-139">NOTES</span></span>

## <span data-ttu-id="63247-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63247-140">RELATED LINKS</span></span>
