---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201449"
---
# <span data-ttu-id="6a399-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="6a399-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="6a399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a399-102">SYNOPSIS</span></span>
<span data-ttu-id="6a399-103">Azure SQL 인스턴스 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="6a399-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a399-104">SYNTAX</span></span>

### <span data-ttu-id="6a399-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a399-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a399-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a399-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a399-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a399-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a399-108">설명</span><span class="sxs-lookup"><span data-stu-id="6a399-108">DESCRIPTION</span></span>
<span data-ttu-id="6a399-109">**Remove-AzSqlInstancePool** cmdlet은 Azure SQL 인스턴스 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="6a399-110">예제</span><span class="sxs-lookup"><span data-stu-id="6a399-110">EXAMPLES</span></span>

### <span data-ttu-id="6a399-111">예제 1: 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="6a399-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="6a399-112">예제 2: 해당 리소스 식별자에 의해 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="6a399-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="6a399-113">예제 3: 인스턴스 풀 개체에 의해 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="6a399-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="6a399-114">이 명령은 instancePool0이라는 인스턴스 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="6a399-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a399-115">PARAMETERS</span></span>

### <span data-ttu-id="6a399-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a399-116">-DefaultProfile</span></span>
<span data-ttu-id="6a399-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a399-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a399-118">-InputObject</span></span>
<span data-ttu-id="6a399-119">제거할 인스턴스 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="6a399-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6a399-120">-Name</span></span>
<span data-ttu-id="6a399-121">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="6a399-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a399-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a399-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a399-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a399-124">-ResourceId</span></span>
<span data-ttu-id="6a399-125">제거할 인스턴스 풀 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="6a399-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a399-126">-Confirm</span></span>
<span data-ttu-id="6a399-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a399-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a399-128">-WhatIf</span></span>
<span data-ttu-id="6a399-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6a399-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a399-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a399-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a399-131">CommonParameters</span></span>
<span data-ttu-id="6a399-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a399-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a399-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a399-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a399-134">입력</span><span class="sxs-lookup"><span data-stu-id="6a399-134">INPUTS</span></span>

### <span data-ttu-id="6a399-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="6a399-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="6a399-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6a399-136">System.String</span></span>

## <span data-ttu-id="6a399-137">출력</span><span class="sxs-lookup"><span data-stu-id="6a399-137">OUTPUTS</span></span>

### <span data-ttu-id="6a399-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="6a399-138">System.Object</span></span>
## <span data-ttu-id="6a399-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a399-139">NOTES</span></span>

## <span data-ttu-id="6a399-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a399-140">RELATED LINKS</span></span>
